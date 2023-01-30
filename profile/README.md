# Nirvati
 
 Nirvati is an in-development project with the goal of adjusting the technology in [Citadel](https://runcitadel.space) for larger deployments and more generic audiences.
 
 Nirvati shares a common goal with Citadel: Being 100% FOSS. Where possible, Nirvati uses existing open source projects and components of Citadel, but extends them for multi-user nodes.
 
 Unlike with Citadel, Bitcoin is not as deeply integrated into Nirvati. Instead, Nirvati tries to build a more generic base projects like Citadel can extend with more apps and features.

## FAQ

### Should I use Nirvati or Citadel?

Citadel is built for individual bitcoiners. Nirvati is built for families, schools, companies and other audiences that may require multi-user capabilities. Generally, smaller nodes should use Citadel, while larger projects should rather start with Nirvati. You will be able to switch from Citadel to Nirvati, but not back.

### Is Nirvati the successor to Citadel?

No. At this point, Nirvati is an experiment. We do not have any intentions of replacing Citadel, merely providing a version of it adjusted for certain audiences.

### Who is building this?

Nirvati is mostly developed by [@AaronDewes](https://github.com/AaronDewes) to play around with various ideas and make adoption of FOSS technologies easier for schools, while still providing all the features Citadel has and not focusing too much on a specific group of people.

## Architecture

Nirvati uses Kubernetes and Helm to orchestrate containers. We try to stay 100% compatible with Citadel `app.yml` files, while extending them with our own Kubernetes-optimized options.

Our backend is written in TypeScript and Rust while our frontend uses [Nuxt.js](https://nuxt.com). We store most data in a PostgreSQL database.

We use [GLAuth](https://glauth.github.io/) as an LDAP server that can be used by apps to integrate with Nirvati users. We are also planning to implement a OAuth server to reduce the amount of times users have to log in. 

## Security & Privacy

We value security & privacy. We regularly validate the security of Nirvati and available software, and already reported multiple vulnerabilities in 3rd party software we utilize. 

You can audit all of our code for yourself, and we try everything we can to avoid security vulnerabilities and patch them as quickly as possible if there are any. If you think there is security vulnerability in any software maintained by Nirvati, please contact us at [security@runcitadel.space](mailto:security@runcitadel.space).
