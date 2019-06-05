# Kittens API

Kittens API is a simple data-producing RESTful API. This project is a part of
[the Odin Project](https://www.theodinproject.com)'s curriculum.

## Getting started

To get started with the app, clone the repo and then install the needed gems:

```
$ bundle install --without production
```

Next, migrate the database:

```
$ rails db:migrate
```

If you want to load sample data, use seeds:

```
$ rails db:seed
```

You are ready to run the app in a local server:

```
$ rails server
```

## Testing Responses

Once the installation is complete and database is seeded, the responses can be tested using `rest-client` gem. The responses can be tested as follows:

```
$ irb
>> require 'rest-client'
>> response = RestClient.get("http://localhost:3000/kittens", accept: :json)
=> <RestClient::Response 200 "[{\"id\":1,\"n...">
>> response = RestClient.get("http://localhost:3000/kittens/1", accept: :json)
=> <RestClient::Response 200 "[{\"id\":1,\"n...">
>> puts response.body
{"id":1,"name":"Garfield","age":3,"cuteness":2,"softness":3,"created_at":"2019-06-05T10:34:38.019Z","updated_at":"2019-06-05T10:34:38.019Z"}
```
