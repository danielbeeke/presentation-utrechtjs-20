###  Easywebrtc

```
    // At peer 1
    EasyWebRtc1.getOffer((offer) => {
        // Send offer via signaling
    });
   
    // At peer 2, recieved 'offer'
    EasyWebRtc2.getAnswer(offer, (answer) => {
        // Send anwser via signaling
    });
    
    // At peer 1 again, received 'answer'
    EasyWebRtc1.acceptAnswer(answer);
    
    EasyWebRtc1.sendMessage('Hello World');
    EasyWebRtc2.on('message', (message) => {})

```