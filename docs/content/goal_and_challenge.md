# Goal and Challenge


Our goal is to create an instrument that improves the drupal project development process. Initially, Drups' purpose is to be the service that listens to every pull request and sets up respective installations with a unique subdomain, where the content and files will be maintained from the general branch. Central idea is that testers and developers can have the exact same instance, full with content for every pull request - even with tiny change.

Unlike most FE applications (that modern tools are working with), in Drupal cases we have different challenges. It is not possible to maintain application state only from the source code. In order to test pull requests properly, testers and developers need content and files, which is not part of the source code and hence can not be pulled automatically. Drups solves this issue and gives development teams necessary tools to control and manage initial databases and files for the project along with unique branches.

Drups is the tool (and service) makes it easy and comfortable for developers and testers to work on a Drupal project. It should not be thought of as a production environment for drupal projects.



