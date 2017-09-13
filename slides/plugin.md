###  Example plugin

Hosted at: http://og-plugins.daniel/webrtc<br>
An introduction may be hosted at index.html<br>
The plugin itself needs to be hosted as plugin.js

```
import Plugin from 'OpenGroup/core/Plugin';
import OgWebRtc from './OgWebRtc.js';

class WebRtc extends Plugin {
    name = 'webrtc';
    config = {};

    constructor (group, config = {}) {
        super();
        Object.assign(this.config, config);
        group.connectionTypes['og-webrtc'] = OgWebRtc;
    }   
}
export default WebRtc;

```