# EaglerProxy in this Eaglercraft client

This client is wired for the EaglerProxy project in
`AV1ZANDUM-ARTIZUM/eaglerproxy`.

## Local testing

1. Start EaglerProxy. Its default WebSocket listener is:
   `ws://127.0.0.1:8080/`
2. Serve this Eaglercraft HTML over **HTTP** for local testing.
3. Open the client.
4. The Multiplayer screen will include **EaglerProxy** automatically.

## Public HTTPS client

A GitHub Pages/HTTPS client cannot safely use the plain `ws://` local endpoint.
Deploy EaglerProxy behind TLS and use its public `wss://` URL.

You can then open this client with:

`?proxy=wss%3A%2F%2FYOUR-PROXY-HOST%2F`

The client will add that address to Multiplayer as **EaglerProxy**.

## Important

The Eaglercraft client only handles the browser-to-EaglerProxy WebSocket connection.
EaglerProxy still needs its upstream Minecraft connection configured separately.

For the Blockbender bridge, the current EaglerProxy setup expects:

`Eaglercraft -> EaglerProxy -> ViaProxy -> play.blockbender.com`

Do not put the Java server address directly into the Eaglercraft client.


<!-- Integration verified against EaglercraftX 1.8 launch-option requirements. -->
