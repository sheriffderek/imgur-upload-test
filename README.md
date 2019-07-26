# imgur-upload-test

Just trying to upload an image somewhere... so that I can send the URL to a printer... (but I don't want to setup a server)

The project this is for primarily - is a Shopify store. It uses jQuery / so, I was using that style of ajax... but no jQuery would be nicer... - / because we're using Vue for some UI sugar / and that drastically simplifies things.

- I tried to do this in codePen - but there's a CORS problem there. / so, I'm making this stand-alone repo to check that out.

## Plan

1. User adds image... which is - then base64 encoded so that we can see it on screen
... but - we shouldn't upload it to imgur yet, right? - because... - what if they change their mind? - It seems like we should do that after they leave that section / or on final confirmation

2. when ready to confirm / upload it to imgur - so that we have URL to get the image from in the product line items. (but for now / any confirmation that this works is fine)

imgur API docs: https://apidocs.imgur.com/?version=latest#c85c9dfc-7487-4de2-9ecd-66f727cf3139

3. - the goal is that we get a URL for where the image lives...

4. - Totally open to some other storage service... the key things just have to be:
* * upload image to a server
* * get a link to that image
* * client can easily get the image
* * doesn't even need to be stored indefinitly... 

## Issues

* CORS

* the response when you DO get the response / doesn't return any URL data - which is the whole point...  / so, if that doesn't work - then we'll need to use some other service.

* there is no transpiler / so - while we're only supporting EDGE and up... / we can't use async await etc. - if the browser can't read it / so , promises - or whatever needs to happen to ensure that things are OK for _no_ build tools.
