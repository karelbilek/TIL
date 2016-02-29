# TIL

Notes about what I learned

Licensed under WTFPL - http://www.wtfpl.net/about/

### js
* in order for fetch to be useful, you should run it with credentials. `fetch(fetchurl, {credentials: 'same-origin'})` is the best I guess.
* JSON.stringify does *not* stringify object keys always in the same order! Sometime it does, sometime it doesn't, it's pretty random frankly. The same objects are stringified the same, *but* different, deeply-equal objects *can be stringified differently*. Use [json-stable-stringify](https://www.npmjs.com/package/json-stable-stringify) instead!!
  * apparently, the order depends on the order in which it was added to the object. Quite surprising to me, since the information is not in the object itself! (Or, at least not visible anywhere)

### git

* `git push --force-with-lease origin master` will push stuff with force, but will check if the stuff at your `origin/master` is the same as at the actual repo. Clever! [more](https://developer.atlassian.com/blog/2015/04/force-with-lease/)

### other web stuff

* I feel I never really understood REST until today. I seriously thought that HTTP methods except `GET`, `POST` and `OPTIONS` are not used ever. But it seems that `DELETE` and `PUT` are actually used in REST API calls pretty often.
    * `PUT` is "indempodent" (word I hear for the first time). It should mean that it could be run multiple times and only the first one has effect.
    * those weird methods (`DELETE`, `PUT`) should have no effect on regular web, but are useful in ajax calls etc
