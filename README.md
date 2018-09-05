Hello World


| Field | Type | Default | Description |
| --- | ---- | ---- | ------ |
| `logLevel` | string or boolean | 'none' | Print log level(debug, info, warn, error, none，false=none, true=debug).
| `announce` | string | 'https://api.cdnbye.com/v1' | The address of tracker server.
| `wsSignalerAddr` | string | 'wss://signal.cdnbye.com/wss' | The address of signal server.
| `wsMaxRetries` | number | 3 | The maximum number of reconnection attempts that will be made by websocket before giving up.
| `wsReconnectInterval` | number | 5 | The number of seconds to delay before attempting to reconnect by websocket.
| `loadTimeout` | number | 3 | Timeout to download a segment from a peer, if exceeded the segment is dropped.
| `maxBufSize` | number | 1024*1024*50 | The max size of binary data that can be stored in the cache.
| `p2pEnabled` | boolean | true | Enable p2p engine.
| `tsStrictMatched` | boolean | false | Drop the query string of ts url while sharing segment to peers.
| `tag` | string | [hlsjs version] | User defined tag which is useful for observing the effect of parameters turning
| `channelId` | function | - | Pass a function to generate channel Id
| `packetSize` | number | 64*1024 | The maximum package size sent by datachannel, 64KB should work with most of recent browsers. Set it to 16KB for older browsers support








        wsSignalerAddr: string              // The address of signal server (default=wss://signal.cdnbye.com/wss)
        wsMaxRetries: number                // The maximum number of reconnection attempts that will be made by websocket before giving up (default=3)
        wsReconnectInterval: number         // The number of seconds to delay before attempting to reconnect by websocket (default=5)
        loadTimeout: number                 // Timeout of downloading by p2p (default=3)
        maxBufSize: number                  // The max size of binary data that can be stored in the cache(default=1024*1024*50)
        p2pEnabled: boolean                 // Enable P2P (default=true)
        tsStrictMatched: boolean            // Drop the query string of ts url while sharing segment to peers (default=false)
        tag: string                         // User defined tag which is useful for observing the effect of parameters turning (default=[hlsjs version])
        // advanced options
        channelId: function                 // Pass a function to generate channel Id (default: see utils/toolFuns)
        dcRequestTimeout: number            // The request timeout of datachannel (default=3)
        dcUploadTimeout: number             // The upload timeout of datachannel (default=3)
        packetSize: number                  // The maximum package size sent by datachannel, 64KB should work with most of recent browsers. Set it to 16KB for older browsers support (default=64*1024).
        enableLogUpload: boolean            // Enable upload logs to server (default=false)
        logUploadAddr: string               // Log upload address (default=wss://api.cdnbye.com/trace)
        logUploadLevel: string              // Log upload level(debug, info, warn, error, none) (default=warn)   
