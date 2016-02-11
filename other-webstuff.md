* I feel I never really understood REST until today. I seriously thought that HTTP methods except `GET`, `POST` and `OPTIONS` are not used ever. But it seems that `DELETE` and `PUT` are actually used in REST API calls pretty often.
    * `PUT` is "indempodent" (word I hear for the first time). It should mean that it could be run multiple times and only the first one has effect.
    * those weird methods (`DELETE`, `PUT`) should have no effect on regular web, but are useful in ajax calls etc
