# REST client for C++

## About
This is a simple REST client for C++. It wraps libcurl for HTTP requests.

## Usage
I tried to keep usage close to the [ruby rest-client][]. So the basic usage is:

    RestClient::method(url, content-type, params);

Examples:

    #include "restclient.h"

    RestClient::response r = RestClient::get("http://url.com")
    RestClient::response r = RestClient::post("http://url.com/post", "text/json", "{"foo": "bla"}")
    RestClient::response r = RestClient::put("http://url.com/put", "text/json", "{"foo": "bla"}")
    RestClient::response r = RestClient::del("http://url.com/delete")

The response is of type RestClient::response and has three attributes:

    RestClient::response.code // HTTP response code
    RestClient::response.body // HTTP response body
    RestClient::response.headers // HTTP response headers

### CMake
A CMake configuration file is provided to ease linking in CMake projects. To make use of this, simple clone this project as a submodule and add the following line into your CMakeLists.txt file:

    add_subdirectory(restclient-cpp)

You can then link against the `restclient-cpp`. Don't forget to link against libcurl too.

## Dependencies
- [libcurl][]
- [gtest][] for development


## Development
- [Issues][]
- [Tracker][]

## Contribute
- Fork the project.
- Make your feature addition or bug fix.
- Add tests for it. This is important so I don't break it in a future version
  unintentionally.
- Commit, do not mess with version
- Send me a pull request. Bonus points for topic branches.


[libcurl]: http://curl.haxx.se/libcurl/
[ruby rest-client]: http://github.com/archiloque/rest-client
[gtest]: http://code.google.com/p/googletest/
[Issues]: https://github.com/mrtazz/restclient-cpp/issues
[Tracker]: https://www.pivotaltracker.com/projects/255177/stories
