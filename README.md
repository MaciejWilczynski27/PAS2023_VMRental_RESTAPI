Spring Boot CRUD web application which allows users to rent virtual machines.(I was responsible for the backend part of it)

- uses MongoDB as it`s main datasource with transactions.
- authorization is realised via JWT token credentials, if user logs out their token is added to the blacklist.
- uses different profile for tests(both integration and unit ones).
- password is kept encoded using BCrypt
- REST API uses DTOs to both receive and send data, so the sensitive data like password is never sent to the client
- data is validated using bean validation, the validator itself is wrapped to throw all the violations in one messagge, so all of them are later cought by the exception handler and sent to the client if necessary
- each user in the system is represented by a different class, which inherits properties from one called User.
