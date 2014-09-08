# Mojolicious::Plugin::Sentry
Mojolicious::Plugin::Sentry is a plugin for the Mojolicious web framework which allow you use Sentry <https://getsentry.com>.

See also [Sentry::Raven](https://metacpan.org/pod/Sentry::Raven) for configuration parameters on init plugin and for use sentryCaptureMessage.

## Usage
    # Mojolicious::Lite
    plugin 'sentry' => {
        sentry_dsn  => 'DSN',
        server_name => 'HOSTNAME',
        logger      => 'root',
        platform    => 'perl',
    };

    # Mojolicious with config
    $self->plugin('sentry' => {
        sentry_dsn  => 'DSN',
        server_name => 'HOSTNAME',
        logger      => 'root',
        platform    => 'perl',
    });

    # template: tmpl/exception.html.ep
    % sentryCaptureMessage $exception;

## See also
[Sentry::Raven](https://metacpan.org/pod/Sentry::Raven)

## Source repository
<https://github.com/likhatskiy/Mojolicious-Plugin-Sentry> 

## Author
Alexey Likhatskiy, <likhatskiy@gmail.com>

## Copyright and licence
Copyright (C) 2014 "Alexey Likhatskiy"

This is free software; you can redistribute it and/or modify it under the same terms as the Perl 5 programming language system itself.