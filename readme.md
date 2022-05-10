

Rennovate fails to resolve the spring boot configuration processor dependency because it thinks my declared alias is the group and my declared group is the name.

When Rennovate creates the pull request, it has the error of `Failed to look up dependency spring.boot.configuration.processor:org.springframework.boot`

In Gradle Version catalogs, we declare them like this:

`library("alias", "group", "name")`

And Rennovate is parsing it and taking `alias:group` instead of ignoring the alias and doing `group:name`


