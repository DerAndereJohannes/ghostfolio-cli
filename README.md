# ghostfolio-cli

[Ghostfolio](https://github.com/ghostfolio/ghostfolio/) is an open source wealth management software built with web technology. This CLI frontend takes advantage of unofficial and official APIs to create a simple and convenient CLI interface to your portfolio.

## Why

Web applications are great at looking nice and providing you with relevant information. However, they have a major downside of being very heavy and inflexible. The CLI application aims to provide a very lightweight alternative to accessing and further processing your data.

## Dependencies

* A bash interpreter `/bin/bash`
* `coreutils`
* `cURL`
* `jq`
* `bc`

## Initialization

The first time you run the script, a config file with defaults will be installed into the CONFIG_FILE location. (default: $HOME/.config/ghostfolio-cli/gfo.conf). The default instance is placed on localhost. If you are using a different instance, change it to the desired instance.

With the correct instance, you can start typing away!

## Examples

Login to your desired Ghostfolio instance

```shell
$ gfo login <secret token>
Ghostfolio bearer token has been updated!
```

Get a smiley face depending on how your portfolio is doing today (positive or negative)

```shell
$ gfo
:-)
```

Get the current status of your portfolio depending on available time ranges (default: 1d)

```shell
$ gfo status ytd
Portfolio Performance change from 2022-10-01 to 2022-11-04: 

   Current Value: 	 12345.00
Net Value Change: 	 169.00 (+.65%)
```

## Organization

The APIs being used in this script are not official and are subject to change at any point. As soon as an API change occurs that breaks the script, a tag will be created which includes the script up to the certain version. Anyone using an older version of Ghostfolio should be able to find a script for their version listed as a tag.

## Roadmap
- [x] Login
- [x] See basic portfolio information
- [ ] See account performance information
- [ ] See account specific positions
- [ ] Get information of specific securities
- [ ] Importing Activities (Official API)
- [ ] Exporting Activities

## Contributing

Pull requests are welcome. The premise of this script is to provide basic information, so keep that in mind. If you have a major feature idea, let's discuss it through the issues page first.

Of course, feel free to fork and create a more interactive experience!

## License

GPL v3

