# Whitepaper

## Overview

Product’s working name is Drups.io.

Drups.io is meant to be the open source project. It will be the collection of software pieces (front-end applications, back-end services and necessary devops scripts) which together assemble the build & deploy automation service for Drupal projects (similar to Netlify build, Vercel and others).

This document describes (1) the problem we face with build & deploy automation when developing drupal projects and (2) in-depth architectural and structural design of the solution along with picked programming languages, necessary tools, libraries and frameworks for implementation.

## Goal and Challenge


Our goal is to create an instrument that improves the drupal project development process. Initially, Drups' purpose is to be the service that listens to every pull request and sets up respective installations with a unique subdomain, where the content and files will be maintained from the general branch. Central idea is that testers and developers can have the exact same instance, full with content for every pull request - even with tiny change.

Unlike most FE applications (that modern tools are working with), in Drupal cases we have different challenges. It is not possible to maintain application state only from the source code. In order to test pull requests properly, testers and developers need content and files, which is not part of the source code and hence can not be pulled automatically. Drups solves this issue and gives development teams necessary tools to control and manage initial databases and files for the project along with unique branches.

Drups is the tool (and service) makes it easy and comfortable for developers and testers to work on a Drupal project. It should not be thought of as a production environment for drupal projects.
