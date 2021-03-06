---
title: "Graphite"
description: "Send metrics to the Graphite time-series database using the plaintext protocol."
product: "Sensu Enterprise"
version: "3.1"
weight: 17
menu:
  sensu-enterprise-3.1:
    parent: integrations
---
**ENTERPRISE: Built-in integrations are available for [Sensu Enterprise][1]
users only.**

- [Overview](#overview)
- [Configuration](#configuration)
  - [Example(s)](#examples)
  - [Integration Specification](#integration-specification)
    - [`graphite` attributes](#graphite-attributes)

## Overview

Send metrics to [Graphite][2], using the plaintext protocol over TCP. The
`graphite` enterprise handler is also capable of sending metrics to [Hosted
Graphite][3], using the `prefix` attribute to prefix metric names with the
Hosted Graphite API key. This handler uses the `output_format` mutator.

## Configuration

### Example(s) {#examples}

The following is an example global configuration for the `graphite` enterprise
handler (integration).

{{< highlight json >}}
{
  "graphite": {
    "host": "graphite.example.com",
    "port": 2003,
    "prefix_source": false,
    "prefix": "production"
  }
}
{{< /highlight >}}

### Integration Specification

#### `graphite` attributes

The following attributes are configured within the `{"graphite": {} }`
[configuration scope][4].

host         | 
-------------|------
description  | The Graphite Carbon host address.
required     | false
type         | String
default      | `127.0.0.1`
example      | {{< highlight shell >}}"host": "carbon.hostedgraphite.com"{{< /highlight >}}

port         | 
-------------|------
description  | The Graphite Carbon port.
required     | false
type         | Integer
default      | `2003`
example      | {{< highlight shell >}}"port": 3003{{< /highlight >}}

prefix_source | 
--------------|------
description   | If the Sensu source (client name) should prefix (added to) the metric names.
required      | false
type          | Boolean
default       | `false`
example       | {{< highlight shell >}}"prefix_source": true{{< /highlight >}}

prefix       | 
-------------|------
description  | A custom metric name prefix - this can be used to prefix the Hosted Graphite API key.
required     | false
type         | String
example      | {{< highlight shell >}}"prefix": "production"{{< /highlight >}}


[?]:  #
[1]:  /sensu-enterprise
[2]:  http://graphite.wikidot.com?ref=sensu-enterprise
[3]:  https://www.hostedgraphite.com?ref=sensu-enterprise
[4]:  /sensu-core/1.2/reference/configuration#configuration-scopes
