# NPM Help!
A live version of this repo is availalbe [here on Laravel Forge](https://npm-help.groveos.net) (which is updated automatically every time I push to this repo). It's bascially this readme, but as an HTML document. I'm also documenting in [this ZipMessage](https://zipmessage.com/groveos/npm-help). Please feel free to comment in the ZipMessage or here in the git repo if you can help (many thanks).

## The gist
I need help understanding NPM and importing/using those packages. NPM packages are totally alien to me. I've been <i>completely baffled for <u>years</u></i>, so I've always just gotten by with vanilla JS, HTML, etc (which is pretty awesome and simple), but I'd like to get better at the fancy NPM thing so I can make use of more third-party tools -- like those made by [UploadCare](https://uploadcare.com/), which appear to require the use of NPM.

So, I'm trying to use [UploadCare's JS upload client](https://github.com/uploadcare/uploadcare-js-api-clients/blob/master/packages/upload-client/README.md) NPM package. I'm pretty sure I've followed <a href="https://uploadcare.com/docs/integrations/javascript/" target="_blank">the installation steps</a> <i>to a T</i>, but the console in browser dev tools (both in local development and here remotely) gives an error, outlined below.

## Here's what I've done so far:
1. Ran `npm install @uploadcare/upload-client` within our project directory
	- That gave us a `node_modules` folder and set up `package-lock.json` and `package.json` files.
2. Wrote the following script in index.html:

```html
<script type='module'>
	import { UploadClient } from '@uploadcare/upload-client';
	const client = new UploadClient({ publicKey: '1234567890' })
</script>
```

That gives the browser console error:

``` error
Uncaught TypeError: Failed to resolve module specifier "@uploadcare/upload-client". Relative references must start with either "/", "./", or "../".
```

**Note**: I've also tried:

``` js
import { UploadClient } from './node_modules/@uploadcare/upload-client'
```

That gives us a 403 forbidden error instead.

---

Please, great people of the Internet, help a brother!

Many thanks,

-*Matthew*

<img src="https://zipmessage-production-misc.s3.amazonaws.com/variants/dwutr0d72r1d8x8et1tipuhf4nn9/0fda02d82170417b1e116aaf4fdecb29471c86941e7ac33ef84152cd616524e2" alt="Matthew's image" width='40' height='40'>