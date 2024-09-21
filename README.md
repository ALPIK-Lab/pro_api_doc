# Pro API v1 documentation

_Updated on September the 21th 2024_

This API allow users to handle data used by Pro web app.

The complete Swagger doc is available at : 
[Pro API Swagger doc](https://api.alpik.fr/pro/v1/swagger/).

## General informations

### Authentication

Authentication is a basic one. To retreive your credentials, you'll have to
connect to [Pro portal](https://pro.alpik.fr). Basic authentication is made of a
username and a password. username is unmutable. Password can be one of those :

* rw primary key : primary key to consume data with no restriction ;
* rw secondary key : secondary key to consume data with no restriction ;
* ro primary key : primary key to consume data in readonly mode ;
* ro secondary key : secondary key to consume data in readonly mode.

For each scope (rw or ro), primary and secondary can be used equaly. It allows
you to roll regulary keys with no service interruption.

### Rate limititation

It is worth noting that this api is rate limited. By default, every account is
limited at 1 request per second. If you need more, please [contact us](#contact-us).

### FIQL

Some requests allow user to complete the request with a FIQL query. FIQL stands
for "Feed Item Query Language", and it is a query language that is used to
filter and search for items in RSS and Atom feeds.

FIQL was designed to be a simple and lightweight language for expressing filter
conditions that can be applied to feed items. It allows users to search for
specific content within feeds based on different criteria, such as keywords,
dates, categories, and authors.

FIQL uses a syntax similar to the URL query string, with different query
parameters separated by ampersands (&). For example, a basic FIQL query for
finding all assets that names "dog" in their designation could look
like this:

```bash
/assets?query=designation=="dog"
```

FIQL also supports more complex queries with logical operators such as "AND",
"OR", and "NOT", as well as comparison operators such as "equals", "contains",
"less than", and "greater than".

Overall, FIQL provides a simple and flexible way for developers and users to
search and filter feed content, making it easier to find the information they
need.

If you plan to use FIQL to request our data, you can read the doc at
[IETF](https://datatracker.ietf.org/doc/html/draft-nottingham-atompub-fiql-00).

## Contact us

If you have any question, requirements, or suggestion, about the API or the
documentation itself, don't hesitate to contact us via email : 
[contact@alpik.fr](mailto:contact@alpik.fr?subject=About%20Pro%20API%20v1).

Otherwise, you can open an issue on our [Github Project](https://github.com/ALPIK-Lab/pro_api_doc/issues).
