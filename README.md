# How to Web Platform in Elm

This is a meta-guide pointing to other resources for the various aspects of the
web platform in [Elm] 0.18. If you're looking for a walkthrough of the language,
I recommend checking out the [official guide].

For most of these, some parts of the platform can be worked with directly in Elm
and some parts fall back to using JS and [ports]. Check out the [roadmap]
document for the future of the web platform in Elm.

## AJAX requests

Use the [Http library]. See the official [guide tutorial on http] and this
[http demo] on Ellie.

## User interaction

For user mouse and keyboard movement in a particular form element or piece of
DOM, use the [HTML event handlers]. To listen to events globally (such as
setting up site-wide keyboard shortcuts), you can subscribe to global
[keyboard events] and [mouse events] via their respective packages.

## Local Storage

You will need to use [ports]. See the [roadmap] document explaining more about
what's in the pipeline for local storage.

## Navigation and History

Programs can be made URL-aware using the [Navigation package]. The package also
allows for manipulating both history and `window.location`.

## Media APIs (Audio and Video)

Some aspects of audio and video can be controlled using custom
[custom event handlers] and [properties]. For other aspects you'll need to use
[ports].

See an example of what can be done in pure Elm in this [video demo] Ellie.

## File manipulation

File uploads must currently be handled in JS via [ports]. Downloads (from a
server) can be triggered by a link that sets the HTML [download attribute].

## Window Manipulation

The [window package] provides functions to query or subscribe to a window's
size. It does not allow changing of the window's size. That must be done via JS
and [ports].

## Querying the DOM

Since `event.target` is a DOM node, you can do some clever things with
[custom event handlers] and decoders to read properties from it. To execute
methods against the DOM or to read properties outside the context of an event,
you'll need to use [ports].

## Non-HTML view layers

Not all visual representations of our model need to be done via HTML. Elm also
supports [svg], [canvas], and [webgl]. These can all be embedded into regular
HTML Elm views. Common uses for these include [data visualizations] and games.

If you're building a game, check out the `#gamedev` channel on the [Elm Slack].

[Elm]: http://elm-lang.org/
[official guide]: https://guide.elm-lang.org/
[ports]: https://guide.elm-lang.org/interop/javascript.html#ports
[roadmap]: https://github.com/elm/projects/blob/master/roadmap.md
[Http library]: http://package.elm-lang.org/packages/elm-lang/http/1.0.0/
[guide tutorial on http]: https://guide.elm-lang.org/architecture/effects/http.html
[http demo]: https://ellie-app.com/k359xZ7cKga1
[HTML event handlers]: http://package.elm-lang.org/packages/elm-lang/html/2.0.0/Html-Events
[keyboard events]: http://package.elm-lang.org/packages/elm-lang/keyboard/1.0.1/Keyboard
[mouse events]: http://package.elm-lang.org/packages/elm-lang/mouse/1.0.1/Mouse
[Navigation package]: http://package.elm-lang.org/packages/elm-lang/navigation/2.1.0/Navigation
[custom event handlers]: http://package.elm-lang.org/packages/elm-lang/html/2.0.0/Html-Events#on
[video demo]: https://ellie-app.com/k32QknpbMPa1
[properties]: http://package.elm-lang.org/packages/elm-lang/html/2.0.0/Html-Attributes#property
[download attribute]: http://package.elm-lang.org/packages/elm-lang/html/2.0.0/Html-Attributes#download
[window package]: http://package.elm-lang.org/packages/elm-lang/window/1.0.1/Window
[svg]: http://package.elm-lang.org/packages/elm-lang/svg/latest
[canvas]: http://package.elm-lang.org/packages/evancz/elm-graphics/latest
[webgl]: http://package.elm-lang.org/packages/elm-community/webgl/latest
[data visualizations]: https://terezka.github.io/line-charts/
[Elm Slack]: https://elmlang.herokuapp.com/
