# Laravel is a Great Framework

In this article, I will explain the benefits of using Laravel as our Framework. This will be both objective and subjective. I also listed the plethora of
features that Laravel has.

## Learning Curve

Laravel is quite easy to learn and easy to setup as well. There are many resources out there to help, such as Laravel Youtube, Laracasts, etc.

As I’m also quite well-versed in Laravel, I can confidently teach our other developers as well.

Laravel have released a very simple yet good [bootcamp](https://bootcamp.laravel.com/), which created a simplified copy of twitter - called chirper.

## Community

Laravel has the biggest community in PHP.
It has 72K stars on its [repository](https://github.com/laravel/laravel), 153K followers on its [twitter](https://twitter.com/laravelphp), 
20K subscribers on its [youtube](https://www.youtube.com/@LaravelPHP) and 30K members on its [discord](https://discord.gg/mPZNm7A).

One of the best open source package maintainer [spatie](https://spatie.be/) is also one of Laravel community member.

The co-founder of Fathom, uses Laravel Vapor to handle millions of requests. https://usefathom.com/blog/does-laravel-scale.

The creator of Rector, recently migrate his sites from Symfony to Laravel. https://tomasvotruba.com/blog/why-I-migrated-this-website-from-symfony-to-laravel

## Front End

Laravel has 3 major choices for Front End that we can choose according to our needs.

### Blade (with Livewire if we need reactivity)

Laravel default templating engine (the equivalent of Twig in Symfony). The default of Laravel installation, the web created with Blade will not be
an SPA, but can have reactivity by adding [Livewire](https://laravel-livewire.com/) in the places that need them.
> This is the easiest stack to use if our developers are more well-versed in Back End (PHP).

### Vue or React (with Inertia)

The most popular choice if we want to have an [SPA](https://developer.mozilla.org/en-US/docs/Glossary/SPA) with full JS framework in the front-end, such as Vue or React, but still have all the benefits
and productivity of Laravel. With the help of [Inertia](https://inertiajs.com/), we can have the Front End and Back End in the same repository (monolith), reducing our
maintenance and development complexities.
> In an upcoming [release](https://github.com/laravel/breeze/pull/267), Laravel will also support a Typescript opt-in for this stack.

### Next.js with Laravel as API

This is the latest addition for the popular [Next.js](https://nextjs.org/). We can separate the Front End and Back End fully by using Next.js as the Front End and using
Laravel only as the API Backend.

## Back End

### Laravel Forge

A paid service provided by Laravel, to help us manage our infrastructure (AWS, Digital Ocean, etc). This could help reduce a lot of manual work
that is needed if we manage our own infrastructure.
> Click [here](https://forge.laravel.com/) for details.

### Laravel Vapor

A paid service provided by Laravel, to help us deploy our web app with a serverless technology, powered by AWS Lambda.
> Click [here](https://vapor.laravel.com/) for details.

### Laravel Octane

A package to help our web to be extra fast (at least twice faster than normal Laravel), by using either [Swoole](https://github.com/swoole/swoole-src) or [RoadRunner](https://roadrunner.dev/). 
This is achieved by saving our framework in the memory once, so that each subsequent requests will skip booting up the framework. 
Road Runner is simpler to setup, but Swoole has more features, such as Concurrent Tasks.
> Click [here](https://laravel.com/docs/10.x/octane) for details.

### Laravel Horizon

A package to help manage and configure our queue, supervisor and workers - provided we use redis for our queue.
> Click [here](https://laravel.com/docs/10.x/horizon) for details.

### Laravel Queue

A native feature of Laravel that can make our jobs or tasks to be run in the background. By default, Laravel supports integrating with database, 
[Amazon SQS](https://aws.amazon.com/sqs/), [Redis](https://redis.io/), and [Beanstalkd](https://beanstalkd.github.io/) drivers.
I personally recommend using Redis driver so that we can monitor them via Horizon, but still use SQS as a failover, in case our Redis is filled.
> Click [here](https://laravel.com/docs/10.x/queues) for details.

### Laravel Pipeline

Pipeline is one of Laravel's less-known features. We can chunk larger tasks into smaller parts in a nice composable way.
> Click for [details](https://laravel.com/docs/10.x/helpers#pipeline) and [examples](https://martinjoo.dev/laravel-pipelines).

## Authentication

### Laravel Sanctum

For a simpler authentication such as personal access token. This is the most recommended for most apps.
> Click [here](https://laravel.com/docs/10.x/sanctum) for details.

### Laravel Passport

For more complex usage, such as a full OAuth2 authentication.
> Click [here](https://laravel.com/docs/10.x/passport) for details.

## Scaffolding

### Laravel Breeze

A simple and recommended scaffolding with basic authentication which can be used with any 3 stacks mentioned in the Front End section above.
> Click [here](https://laravel.com/docs/10.x/starter-kits#laravel-breeze) for details.

### Laravel Jetstream

A more sophisticated scaffolding with extra features, such as Two Factor Authentication, Team Management, etc. This scaffolding only supports
Blade + Livewire and Inertia + Vue option.
> Click [here](https://jetstream.laravel.com/3.x/introduction.html) for details.

## Third Party Integration

### Laravel Echo

A package to add websocket broadcasting feature to our web app. Can be integrated with [Pusher](https://pusher.com/channels), [Ably](https://ably.com/), 
[laravel-websockets](https://beyondco.de/docs/laravel-websockets/getting-started/introduction) and [soketi](https://docs.soketi.app/)
> Click [here](https://laravel.com/docs/10.x/broadcasting) for details.

### Laravel Scout

A package to add Full Text Search feature to our web app. Can be integrated with [Algolia](https://www.algolia.com/), [MeiliSearch](https://www.meilisearch.com/), and MySQL / PostgreSQL
> Click [here](https://laravel.com/docs/10.x/scout) for details.

### Laravel Socialite

A package to help integration with 3rd party logins, such as Google, Twitter, Facebook, Github, etc.
> Click [here](https://laravel.com/docs/10.x/socialite) for details.

### Laravel Cashier

A package to help integration with either [Stripe](https://stripe.com/) or [Paddle](https://www.paddle.com/).
> Click [here](https://laravel.com/docs/10.x/billing) for details.

## Developer Tools

### Laravel Valet

The most recommended way to develop Laravel if we use MacOS.
> Click [here](https://laravel.com/docs/10.x/valet) for details.

### Laravel Sail

A simple command line to help our development using [Docker](https://www.docker.com/). This is the recommended way if we have many developers using different OS.
> Click [here](https://laravel.com/docs/10.x/sail) for details.

### Laravel Homestead

A [vagrant](https://www.vagrantup.com/) virtual box especially made for Laravel development. This can also be used for many developers using different OS.
> Click [here](https://laravel.com/docs/10.x/homestead) for details.

### Laravel Telescope

A very detailed and helpful dashboard to monitor our web app. It can be used in local only, or used in other environments, provided we add the
proper authentication and authorization in place.
> Click [here](https://laravel.com/docs/10.x/telescope) for details.

### Laravel Dusk

A package to help us creating Browser Tests, that simulate real users navigating our web app. Good for User Acceptance Test.
> Click [here](https://laravel.com/docs/10.x/dusk) for details.

### Laravel Pint

A package built on top of PHP CS Fixer, but with simpler configuration and fine-tuned for Laravel. One of the latest features is `--dirty` option
that can be used in our local when developing.

It will be much faster than running PHP CS Fixer locally to scan & fix our whole repository.
> Click [here](https://laravel.com/docs/10.x/pint) for details.

### Laravel Shift

A paid service to help upgrading our Laravel, PHP and dependencies versions. By incrementally upgrading our code base, we can stay up to
date to the latest features, reducing tech debt and preventing our code base to become a “legacy” code base.
> Click [here](https://laravelshift.com/) for details.


## Final Thoughts

Laravel is a great framework and a joy to work with. Easy to learn for juniors and powerful for seniors.

Instead of creating a lot of micro services, I would personally suggest that we use Laravel as a modern monolith and maintain it with proper
structuring (this [article](https://stitcher.io/blog/laravel-beyond-crud-01-domain-oriented-laravel) as example) and tools (such as PHPStan, Rector and Laravel Shift) in place.

For scaling our load, we can leverage our infrastructure instead of using micro services. Either using AWS Autoscaling or AWS Lambda via
Laravel Vapor. We can also use Laravel Octane to boost the performance even more.
