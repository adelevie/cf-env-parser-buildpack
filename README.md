# cf-env-parser-buildpack

A buildpack designed to pull environment variables out of `VCAP_SERVICES` when using a user-provided services on Cloud Foundry.

## Usage

This buildpack should be used as part of a [multi-buildpack setup](https://github.com/ddollar/heroku-buildpack-multi).

If an app has user-provided services, Cloud Foundry provides information about those services in an environment variable called `VCAP_SERVICES`. It's JSON, and you can read more about it in the [CF docs](http://docs.cloudfoundry.org/devguide/deploy-apps/environment-variable.html#VCAP-SERVICES). This buildpack pulls out the `name` and `credentials` values, and provides them as separate environment variables in the format `name_credential-key=credential-value`.

## Contributing

See [CONTRIBUTING](CONTRIBUTING.md) for additional information.

### Branch flow

- Main branch: `release`
- Development branch: `develop`

## Public domain

This project is in the worldwide [public domain](LICENSE.md). As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0 dedication. By submitting a pull request, you are agreeing to comply with this waiver of copyright interest.
