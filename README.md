Hello World


| Field | Type | Default | Description |
| :-: | :-: | :-: | :-: |
| `logLevel` | string or boolean | 'none' | Print log level(debug, info, warn, error, none，false=none, true=debug).
| `announce` | string | 'https://api.cdnbye.com/v1' | The address of tracker server.
| `wsSignalerAddr` | string | 'wss://signal.cdnbye.com/wss' | The address of signal server.
| `wsMaxRetries` | number | 3 | The maximum number of reconnection attempts that will be made by websocket before giving up.
| `wsReconnectInterval` | number | 5 | The number of seconds to delay before attempting to reconnect by websocket.
| `loadTimeout` | number | 3 | Timeout to download a segment from a peer, if exceeded the segment is dropped.
| `maxBufSize` | number | 1024 * 1024 * 50 | The max size of binary data that can be stored in the cache.
| `p2pEnabled` | boolean | true | Enable or disable p2p engine.
| `tsStrictMatched` | boolean | false | Drop the query string of ts url while sharing segment to peers.
| `tag` | string | [hlsjs version] | User defined tag which is useful for observing the effect of parameters turning.
| `channelId` | function | - | Pass a function to generate channel Id.
| `packetSize` | number | 64 * 1024 | The maximum package size sent by datachannel, 64KB should work with most of recent browsers. Set it to 16KB for older browsers support.



| 字段 | 类型 | 默认值 | 描述 |
| :-: | :-: | :-: | :-: |
| `logLevel` | string or boolean | 'none' | log的等级，分为debug、info、warn、error、none，设为true等于debug，设为false等于none。
| `announce` | string | 'https://api.cdnbye.com/v1' | tracker服务器地址。
| `wsSignalerAddr` | string | 'wss://signal.cdnbye.com/wss' | 信令服务器地址。
| `wsMaxRetries` | number | 3 |websocket连接重试次数。
| `wsReconnectInterval` | number | 5 | websocket重连时间间隔。
| `loadTimeout` | number | 3 | p2p下载的超时时间。
| `maxBufSize` | number | 1024 * 1024 * 50 | p2p缓存的最大数据量。
| `p2pEnabled` | boolean | true | 是否开启P2P。
| `tsStrictMatched` | boolean | false | p2p传输的ts是否要严格匹配（去掉查询参数）。
| `tag` | string | [hlsjs version] | 用户自定义标签，可用于在后台查看参数调整效果。
| `channelId` | function | - | 标识channel的字段，同一个channel的用户可以共享数据。
| `packetSize` | number | 64 * 1024 | 每次通过datachannel发送的包的大小，64KB适用于较新版本的浏览器，如果要兼容低版本浏览器可以设置成16KB。




