### ws的api

当接收到某个websocket个用户退出时，服务端不会处理这个过程，但是客户端如果认为这是个错误的退出，就会向服务端连接

当一个ws连接断掉，ws会广播一个对象`{code：4：id：id}`

当一个ws连接上，那么ws就会广播一个对象`{code:2:id:id}`

当有数据传入，ws广播一个对象`{code:3,id:id,message}`,如果数据来自自己，那么就`{code:1,id:id,message}`

 所有的数据都会被装在一个对象的`data`属性内