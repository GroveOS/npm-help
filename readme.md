<h1>NPM Help!</h1>
<p>NPM packages are totally alien to me. I've been <i>completely baffled for <u>years</u></i>, so I've always just gotten by with vanilla JS, HTML, etc (which is pretty awesome and simple), but I'd like to get better at the fancy NPM thing so I can make use of more third-party tools -- like those made by UploadCare, which appear to require the use of NPM.</p>
<p>So, I're trying to use UploadCare's JS upload client NPM package. I'm pretty sure I've followed <a href="https://uploadcare.com/docs/integrations/javascript/" target="_blank">the installation steps</a> <i>to a T</i>, but the console in browser dev tools (both in local development and here remotely) gives an error, outlined below.</p>
<h2>Here's what I've done so far:</h2>
<ol>
	<li>Ran <pre>npm install @uploadcare/upload-client</pre> within our project directory
		<ul>
			<li>That gave us a <span class='monospace'>node_modules</span> folder and set up <span class='monospace'>package-lock.json</span> and <span class='monospace'>package.json</span> files.</li>
		</ul>
	</li>
	<li>Wrote the following script in index.html (this file)<br />
		<pre>&lt;script type='module'&gt;<br />	import { UploadClient } from '@uploadcare/upload-client';<br />	const client = new UploadClient({ publicKey: '1234567890' })<br />&lt;/script&gt;</pre>
</ol>
<p>That gives us the browser console error: <div style="background: #eee;padding: 24px;font-family: monospace;max-width:360px;overflow:wrap; color:maroon;">Uncaught TypeError: Failed to resolve module specifier "@uploadcare/upload-client". Relative references must start with either "/", "./", or "../".</div></p>
<p><b>Note:</b> I've also tried:</p>
<pre>import { UploadClient } from './node_modules/@uploadcare/upload-client'</pre>
<p>That gives us a 403 forbidden error instead.</p>
---
<p>Please, great people of the Internet, help a brother!</p>
<div style="display:flex;align-items:center;">
	<img src="https://zipmessage-production-misc.s3.amazonaws.com/variants/dwutr0d72r1d8x8et1tipuhf4nn9/0fda02d82170417b1e116aaf4fdecb29471c86941e7ac33ef84152cd616524e2" alt="Matthew's image" style="border-radius:50%; margin-right:12px;" width='40' height='40'>
	<p>Many thanks,<br /><i>Matthew</i></p>
</div>