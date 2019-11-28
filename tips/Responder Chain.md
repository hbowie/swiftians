Title:  Responder Chain

Tags:   AppKit, responder

Link:   https://developer.apple.com/documentation/uikit/touches_presses_and_gestures/using_responders_and_the_responder_chain_to_handle_events

Text:   Apple Developer Docs

Type:   Concept

Body: 

In macOS and Cocoa, a user action may trigger an event that will be handled by the First Responder, meaning the first Cocoa object willing and able to respond to the event, starting with the view closest to the one generating the event, proceeding upwards to higher level objects until an object steps up to the job. 

The responder chain proceeds in roughly the following order:

View -> Parent View -> View Controller -> Window -> Window Controller -> App Delegate

