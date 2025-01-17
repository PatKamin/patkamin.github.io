---
draft: false
layout: "library"
slider_enable: true
description: ""
disclaimer: "The contents of this web site and the associated <a href=\"https://github.com/pmem\">GitHub repositories</a> are BSD-licensed open source."
aliases: ["rpma_conn_cfg_set_compl_channel.3.html"]
title: "librpma | PMDK"
header: "librpma API version 0.14.0"
---
{{< manpages >}}

[comment]: <> (SPDX-License-Identifier: BSD-3-Clause)
[comment]: <> (Copyright 2020-2022, Intel Corporation)

NAME
====

**rpma\_conn\_cfg\_set\_compl\_channel** - set if the completion event
channel can be shared by CQ and RCQ

SYNOPSIS
========

          #include <librpma.h>

          struct rpma_conn_cfg;
          int rpma_conn_cfg_set_compl_channel(struct rpma_conn_cfg *cfg,
                          bool shared);

DESCRIPTION
===========

**rpma\_conn\_cfg\_set\_compl\_channel**() sets if the completion event
channel can be shared by CQ and RCQ or not. The completion event channel
is not shared by CQ and RCQ by default. See **rpma\_conn\_cfg\_new**(3)
for details.

RETURN VALUE
============

The **rpma\_conn\_cfg\_set\_compl\_channel**() function returns 0 on
success or a negative error code on failure.

ERRORS
======

**rpma\_conn\_cfg\_set\_compl\_channel**() can fail with the following
error:

-   RPMA\_E\_INVAL - cfg is NULL

SEE ALSO
========

**rpma\_conn\_cfg\_new**(3), **rpma\_conn\_wait**(3),
**rpma\_conn\_cfg\_get\_compl\_channel**(3), **librpma**(7) and
https://pmem.io/rpma/
