docker-seyren
=============

A dockerized [Seyren](https://github.com/scobal/seyren) Container

## Usage

```
# Run MongoDB
docker run -d --name mongodb dockerfile/mongodb

# Run Seyren and link MongoDB
docker run -d -p 8080:8080 --name seyren --link mongodb:mongodb -i -t usman/docker-seyren http://[GRAPHITE_URL]
```
Then point your browser at [http://localhost:8080/](http://localhost:8080/)

or [http://192.168.59.103:8080/](http://192.168.59.103:8080/) if you are using boot2docker

## Building

To build the image, simply invoke

    docker build github.com/usmanismail/docker-seyren

A prebuilt container is also available in the docker index

    docker pull usman/docker-seyren
    
## Author

  * Usman Ismail (<usman@techtraits.com>)

## LICENSE

Copyright 2014 Usman Ismail

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
    
