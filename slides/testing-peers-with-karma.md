###  Testing peers with Karma

* Multiple groups running in a browser
* Karma start firefox and chrome
* https://github.com/computmaxer/karma-jspm

```
it('should create an answer from an offer', (done) => {
    EasyWebRtc2.getAnswer(EasyWebRtc1Offer, (answer) => {
        if (answer && answer.type) {
            expect(answer.type).toEqual('answer');
            EasyWebRtc2Answer = answer;
            done();
        }
    });
});

it('should run a callback when created', (done) => {
    EasyWebRtc1.on('connected', () => {
        done();
    });
    EasyWebRtc1.acceptAnswer(EasyWebRtc2Answer);
});
```