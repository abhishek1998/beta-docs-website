---
layout: default
title: Data Parsing Rules
nav_order: 7
has_children: true
permalink: /docs/data-parsing-rules
---

# Data Parsing Rule Based on Data Format

You can select in which format you receive emails on inbound email address and based on that you can select the appropriate data format.
{: .fs-6 .fw-300 }

{: .important }
You need to choose correct email data format for successful data parsing.

## Default Data Format

By default, data parsing will work if the email are coming in key-value pair format with a separator between keys and values.

For example,

```text
Name:: William
Phone:: 1234567890
Email Address:: william@email.com
Job Title:: Sales Rep
```

If you're receiving data in any other format then you need to enable following data parsing rules.