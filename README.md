[![](https://raw.github.com/HaxeFlixel/haxeflixel.com/master/src/files/images/flixel-logos/HaxeFlixel.png)](http://haxeflixel.com/)

[flixel](https://github.com/HaxeFlixel/flixel) | [addons](https://github.com/HaxeFlixel/flixel-addons) | [ui](https://github.com/HaxeFlixel/flixel-ui) | [demos](https://github.com/HaxeFlixel/flixel-demos) | [tools](https://github.com/HaxeFlixel/flixel-tools) | [templates](https://github.com/HaxeFlixel/flixel-templates) | [docs](https://github.com/HaxeFlixel/flixel-docs) | [haxeflixel.com](https://github.com/HaxeFlixel/haxeflixel.com)

[![CI](https://img.shields.io/github/actions/workflow/status/HaxeFlixel/flixel/main.yml?branch=dev&logo=github)](https://github.com/HaxeFlixel/flixel/actions?query=workflow%3ACI)
[![Discord](https://img.shields.io/discord/162395145352904705.svg?logo=discord)](https://discordapp.com/invite/rqEBAgF)
[![Haxelib Version](https://badgen.net/haxelib/v/flixel)](https://lib.haxe.org/p/flixel)
[![Haxelib Downloads](https://badgen.net/haxelib/d/flixel?color=blue)](https://lib.haxe.org/p/flixel)
[![Haxelib License](https://badgen.net/haxelib/license/flixel)](LICENSE.md)
[![Patreon](https://img.shields.io/badge/donate-patreon-blue.svg)](https://www.patreon.com/haxeflixel) 

[![](images/showcase.png)](https://haxeflixel.com/showcase)

## Codename Metal fork (instancing support)

**This is the Flixel fork used by [Codename-Metal](https://github.com/TheComingUnitys/Codename-Metal)**
(based on Flixel 5.3.0).  Flixel sprites are OpenFL `Bitmap` objects, so the instanced
bitmap batching lives in
[openfl-metal](https://github.com/TheComingUnitys/openfl-metal).  This fork adds the
`FlxG.metalInstancing` toggle:

```haxe
FlxG.metalInstancing = true; // enable the Metal batch (default false / opt-in)
```

### Use it with Codename-Metal

```sh
git clone https://github.com/TheComingUnitys/openfl-metal.git
git clone https://github.com/TheComingUnitys/flixel-metal.git

cd /path/to/Codename-Metal/CodenameEngine-1.0.1
haxelib dev openfl  /path/to/openfl-metal
haxelib dev flixel  /path/to/flixel-metal
```

Then build with the Metal backend as described in Codename-Metal's README
(`-Dmetal -Dmetal_instancing`; the engine's `project.xml` enables both).  Do not mix this
fork with Flixel 6.x: Codename Engine 1.0.1 uses the 5.3.0 API.

Without the `metal_instancing` define this fork behaves like upstream Flixel 5.3.0.

### Reverting to upstream Flixel

```sh
haxelib dev flixel      # remove the development directory link
haxelib set flixel git  # restore the copy vendored by Codename-Metal
```

See `METAL-INSTANCING.md` for details.

---

## Links

Here are the most important links to get you started with HaxeFlixel:

- [Getting Started](https://haxeflixel.com/documentation/getting-started/)
- [Documentation](https://haxeflixel.com/documentation)
- [API](https://api.haxeflixel.com/)
- [Community](https://haxeflixel.com/documentation/community/)

If you want to contribute code or report an issue, please check our [CONTRIBUTING.md](https://github.com/HaxeFlixel/flixel/blob/dev/.github/CONTRIBUTING.md).

## Platforms

Thanks to being built on top of [Haxe](https://haxe.org/) and [OpenFL](http://www.openfl.org/), HaxeFlixel can target the following platforms _natively_:

![](images/platforms.png)

## About

HaxeFlixel has its roots in the original [ActionScript 3 version of Flixel](https://github.com/AdamAtomic/flixel), created by [Adam “Atomic” Saltsman](http://www.adamatomic.com/). It was started by [Alexander Hohlov](https://github.com/beeblerox) in 2011, initially as a straightforward Haxe port of the AS3 codebase and Richard Davey's [Flixel Power Tools](http://www.photonstorm.com/flixel-power-tools).

Thanks to the efforts of the [core team](https://github.com/orgs/HaxeFlixel/people) as well as [over 100 contributors](https://github.com/HaxeFlixel/flixel/graphs/contributors), today's version of HaxeFlixel far surpasses the capabilities of the original. Not only has the core engine seen many substantial improvements and new features, there is also a far richer ecosystem with additional libaries and [over 80 demo projects](https://github.com/HaxeFlixel/flixel-demos) to learn from.
