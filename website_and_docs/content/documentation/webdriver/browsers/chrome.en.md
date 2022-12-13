---
title: "Chrome specific functionality"
linkTitle: "Chrome"
weight: 4
description: >-
    These are capabilities and features specific to Google Chrome browsers.
aliases: [
"/documentation/capabilities/chromium"
]
---

By default, Selenium 4 is compatible with Chrome v75 and greater. Note that the version of
the Chrome browser and the version of chromedriver must match the major version.

## Options

Capabilities common to all browsers are described on the [Options page]({{< ref "../drivers/options.md" >}}).

Capabilities unique to Chrome can be found at Google's page for [Capabilities & ChromeOptions](https://chromedriver.chromium.org/capabilities)

Starting a Chrome session with basic defined options looks like this:

{{< tabpane code=false langEqualsHeader=true >}}
{{< tab header="Java" >}}
{{< gh-codeblock path="/examples/java/src/test/java/dev/selenium/browsers/ChromeTest.java#L18-L19" >}}
{{< /tab >}}
{{% tab header="Python" %}}
{{< gh-codeblock path="/examples/python/tests/browsers/test_chrome.py#L6-L7" >}}
{{% /tab %}}
{{< tab header="CSharp" >}}
{{< gh-codeblock path="/examples/dotnet/SeleniumDocs/Browsers/ChromeTest.cs#L12-L13" >}}
{{< /tab >}}
{{< tab header="Ruby" >}}
{{< gh-codeblock path="/examples/ruby/spec/browsers/chrome_spec.rb#L7-L8" >}}
{{< /tab >}}
{{< tab header="JavaScript" >}}
{{< gh-codeblock path="/examples/javascript/test/getting_started/openChromeTest.spec.js#L10-L14">}}
{{< /tab >}}
{{< tab header="Kotlin" >}}
{{< badge-code >}}
{{< /tab >}}
{{< /tabpane >}}

Here are a few common use cases with different capabilities:

### Arguments

The `args` parameter is for a list of [Command Line Switches](https://peter.sh/experiments/chromium-command-line-switches/)
used when starting the browser.
Commonly used args include `--start-maximized` and `user-data-dir=/tmp/temp_profile`

Add an argument to options:

{{< alert-code />}}

### Start browser in a specified location

The `binary` parameter takes the path of an alternate location of browser to use. With this parameter you can
use chromedriver to drive various Chromium based browsers.

Add a browser location to options:

{{< alert-code />}}

### Add extensions

The `extensions` parameter accepts crx files

Add an extension to options:

{{< alert-code />}}

### Keeping browser open

Setting the `detach` parameter to true will keep the browser open after the driver process has been quit.

Add a binary to options:

{{< alert-code />}}

### Excluding arguments

Chrome adds various arguments, if you do not want those arguments added, pass them into `excludeSwitches`.
A common example is to turn the popup blocker back on.

Set excluded arguments on options:

{{< alert-code />}}

## Casting

You can drive Chrome Cast devices, including sharing tabs

{{< alert-code />}}

## Network conditions

You can simulate various network conditions.

{{< alert-code />}}

## Logs

{{< alert-code />}}

## Permissions

{{< alert-code />}}

## DevTools

See the [Chrome DevTools]({{< ref "../bidirectional/chrome_devtools.md" >}}) section for more information about using Chrome DevTools