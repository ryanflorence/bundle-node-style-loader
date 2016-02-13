# bundle loader for webpack with node-style callback signature

Identical to [bundle-loader](https://github.com/webpack/bundle-loader) but has node-style callback signatures.

## Installation

```
npm install bundle-node-style-loader
```

## Usage

```js
import loadThing from 'bundle?lazy./thing'

// instead of the bundle loader api:
loadThing((thing) => {})

// you get node-style callbacks:
loadthing((err, thing) => {})
```

It always sends `null` for the error, but this way it pairs well with
other libs, like, say ... React Router:

```js
import loadInvoices from 'bundle?lazy!./Invoices'
<Route path="/stuff" getComponent={loadInvoices}/>
```

## License

MIT (http://www.opensource.org/licenses/mit-license.php)
