# git-up [![Support this project][donate-now]][paypal-donations]

A low level git url parser.

## Installation

```sh
$ npm i git-up
```

## Example

```js
// Dependencies
var GitUp = require("git-up");

console.log(GitUp("git@github.com:IonicaBizau/node-parse-url.git"));
// => {
//     protocols: []
//   , port: null
//   , resource: "github.com"
//   , user: "git"
//   , pathname: "/IonicaBizau/node-parse-url.git"
//   , hash: ""
//   , search: ""
//   , href: "git@github.com:IonicaBizau/node-parse-url.git"
//   , protocol: "ssh"
// }

console.log(GitUp("https://github.com/IonicaBizau/node-parse-url.git"));
// => {
//     protocols: [ "https" ]
//   , port: null
//   , resource: "github.com"
//   , user: ""
//   , pathname: "/IonicaBizau/node-parse-url.git"
//   , hash: ""
//   , search: ""
//   , href: "https://github.com/IonicaBizau/node-parse-url.git"
//   , protocol: "https"
// }
```

## Documentation

### `GitUp(input)`
Parses the input url.

#### Params
- **String** `input`: The input url.

#### Return
- **Object** An object containing the following fields:
 - `protocols` (Array): An array with the url protocols (usually it has one element).
 - `port` (null|Number): The domain port.
 - `resource` (String): The url domain (including subdomains).
 - `user` (String): The authentication user (usually for ssh urls).
 - `pathname` (String): The url pathname.
 - `hash` (String): The url hash.
 - `search` (String): The url querystring value.
 - `href` (String): The input url.
 - `protocol` (String): The git url protocol.
 - `token` (String): The oauth token (could appear in the https urls).

## How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].

## Where is this library used?
If you are using this library in one of your projects, add it in this list. :sparkles:

 - [`git-url-parse`](https://github.com/IonicaBizau/node-git-url-parse)

## License

[KINDLY][license] © [Ionică Bizău][website]

[license]: http://ionicabizau.github.io/kindly-license/?author=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica@gmail.com%3E&year=2015

[website]: http://ionicabizau.net
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md