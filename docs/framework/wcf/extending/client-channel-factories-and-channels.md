---
title: '클라이언트: 채널 팩터리 및 채널'
ms.date: 03/30/2017
ms.assetid: ef245191-fdab-4468-a0da-7c6f25d2110f
ms.openlocfilehash: a42042eaf9a8bc5461f680e3cf8dc5fcc78cebb5
ms.sourcegitcommit: b7763f3435635850a76d4cbcf09bdce6c019208a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/25/2018
ms.locfileid: "34483556"
---
# <a name="client-channel-factories-and-channels"></a>클라이언트: 채널 팩터리 및 채널
이 항목에서는 채널 팩터리 및 채널 만들기에 대해 설명합니다.  
  
## <a name="channel-factories-and-channels"></a>채널 팩터리 및 채널  
 채널 팩터리는 채널을 만듭니다. 채널 팩터리에서 만든 채널은 메시지를 보내는 데 사용됩니다. 이러한 채널은 위의 계층에서 메시지를 가져와서 필요한 모든 처리 작업을 수행한 다음 메시지를 아래 계층으로 보냅니다. 다음 그래픽에서는 이 프로세스를 보여 줍니다.  
  
 ![클라이언트 팩터리 및 채널](../../../../docs/framework/wcf/extending/media/wcfc-wcfchannelsigure2highlevelfactgoriesc.gif "wcfc_WCFChannelsigure2HIghLevelFactgoriesc")  
채널 팩터리가 채널을 만듭니다.  
  
 닫힌 채널 팩터리는 만든 채널 중에서 아직 닫히지 않은 채널을 닫습니다. 여기서는 채널 수신기가 닫혀 있기 때문에 모델이 비대칭이며, 새 채널 승인만 중지하고 기존 채널은 메시지 수신을 계속할 수 있도록 열린 상태로 유지합니다.  
  
 WCF는이 프로세스에 대 한 기본 클래스 도우미를 제공합니다. (이 항목에서 설명 하는 채널 도우미 클래스 다이어그램을 참조 하십시오. [채널 모델 개요](../../../../docs/framework/wcf/extending/channel-model-overview.md).)  
  
-   <xref:System.ServiceModel.Channels.CommunicationObject> 클래스 구현 <xref:System.ServiceModel.ICommunicationObject> 의 2 단계에서 설명한 상태 시스템을 적용 하 고 [개발 채널](../../../../docs/framework/wcf/extending/developing-channels.md)합니다.  
  
-   <xref:System.ServiceModel.Channels.ChannelManagerBase> 클래스는 <xref:System.ServiceModel.Channels.CommunicationObject>를 구현하고 <xref:System.ServiceModel.Channels.ChannelFactoryBase?displayProperty=nameWithType> 및 <xref:System.ServiceModel.Channels.ChannelListenerBase?displayProperty=nameWithType>에 대한 통합 기본 클래스를 제공합니다. <xref:System.ServiceModel.Channels.ChannelManagerBase> 클래스는 <xref:System.ServiceModel.Channels.ChannelBase>을 구현하는 기본 클래스인 <xref:System.ServiceModel.Channels.IChannel>와 함께 사용됩니다.
  
-   <xref:System.ServiceModel.Channels.ChannelFactoryBase> 클래스 구현 <xref:System.ServiceModel.Channels.ChannelManagerBase> 및 <xref:System.ServiceModel.Channels.IChannelFactory> 하 고 통합 된 `CreateChannel` 하나에 오버 로드 `OnCreateChannel` 추상 메서드.
  
-   <xref:System.ServiceModel.Channels.ChannelListenerBase> 클래스는 <xref:System.ServiceModel.Channels.IChannelListener>을 구현합니다. 이 클래스는 기본 상태 관리를 담당합니다. 
  
 다음 논의 기반으로 [전송: UDP](../../../../docs/framework/wcf/samples/transport-udp.md) 샘플.  
  
### <a name="creating-a-channel-factory"></a>채널 팩터리 만들기  
 `UdpChannelFactory`는 <xref:System.ServiceModel.Channels.ChannelFactoryBase>에서 파생됩니다. 샘플에서는 메시지 인코더의 메시지 버전에 액세스할 수 있도록 <xref:System.ServiceModel.Channels.ChannelFactoryBase.GetProperty%2A>를 재정의합니다. 또한 상태 시스템이 전환될 때 <xref:System.ServiceModel.Channels.ChannelFactoryBase.OnClose%2A>의 인스턴스를 중지하도록 <xref:System.ServiceModel.Channels.BufferManager>를 재정의합니다.  
  
#### <a name="the-udp-output-channel"></a>UDP 출력 채널  
 `UdpOutputChannel`은 <xref:System.ServiceModel.Channels.IOutputChannel>을 구현합니다. 생성자는 인수의 유효성을 검사하여 전달되는 <xref:System.Net.EndPoint>를 기반으로 대상 <xref:System.ServiceModel.EndpointAddress> 개체를 구성합니다.  
  
 <xref:System.ServiceModel.Channels.CommunicationObject.OnOpen%2A>을 재정의하면 이 <xref:System.Net.EndPoint>에 메시지를 보내는 데 사용되는 소켓이 생성됩니다.  
  
 `this.socket = new Socket(`  
  
 `this.remoteEndPoint.AddressFamily,`  
  
 `SocketType.Dgram,`  
  
 `ProtocolType.Udp`  
  
 `);`  
  
 채널이 정상적 또는 비정상적으로 닫힐 수 있습니다. 채널이 정상적으로 닫히면 소켓이 닫히고 기본 클래스 `OnClose` 메서드가 호출됩니다. 이 때 예외가 throw되면 인프라가 `Abort`를 호출하여 채널을 정리합니다.  
  
```  
this.socket.Close();  
base.OnClose(timeout);  
```  
  
 구현 `Send()` 및 `BeginSend()` / `EndSend()`합니다. 그러면 두 개의 기본 섹션으로 분할됩니다. 먼저 메시지를 바이트 배열로 serialize합니다.  
  
```  
ArraySegment<byte> messageBuffer = EncodeMessage(message);  
```  
  
 그런 다음 네트워크를 통해 결과 데이터를 보냅니다.  
  
```  
this.socket.SendTo(  
  messageBuffer.Array,   
  messageBuffer.Offset,   
  messageBuffer.Count,   
  SocketFlags.None,   
  this.remoteEndPoint  
);  
```  
  
## <a name="see-also"></a>참고 항목  
 [채널 개발](../../../../docs/framework/wcf/extending/developing-channels.md)
