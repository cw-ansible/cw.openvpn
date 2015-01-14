<!--

---
lang: american
---
-->

[![Build Status](https://travis-ci.org/cw-ansible/cw.openvpn.svg?branch=master)](https://travis-ci.org/cw-ansible/cw.openvpn)
[![Tweet this](http://img.shields.io/badge/%20-Tweet-00aced.svg)](https://twitter.com/intent/tweet?tw_p=tweetbutton&via=renard_0&url=https%3A%2F%2Fgithub.com%2Fcw-ansible%2Fcw.openvpn&text=Install%20and%20configure%20%40OpenVPN%20using%20%23ansible.)
[![Follow me on twitter](http://img.shields.io/badge/Twitter-Follow-00aced.svg)](https://twitter.com/intent/follow?region=follow_link&screen_name=renard_0&tw_p=followbutton)


# OpenVPN

Install and configure [OpenVPN](http://openvpn.net) services.

## Usage

Include the `cw.openvpn` module to your playbook.

## Description

This role install *OpenVPN* (both client and server) on hosts defined in
`openvpn_config`. You can create how many VPNs as you want.


A VPN consists of a server and clients. *OpenVPN* can be used in *TCP* or
*UDP* (prefered for performances) mode. This configuration allows you to use
both modes for a VPN (same private IP range).

For example a VPN range is `A.B.C.0/24` the IP addresses are used:

- `A.B.C.1` - `A.B.C.2`: Server in *UDP* mode
- `A.B.C.3` - `A.B.C.4`: Server in *TCP* mode
- `A.B.C.5` - `A.B.C.6`: First client
- `A.B.C.7` - `A.B.C.8`: Second client
- ...


## Configuration

See specific documentation in `defaults/main.yml`

## Copyright

Author: Sébastien Gross `<seb•ɑƬ•chezwam•ɖɵʈ•org>` [@renard_0](https://twitter.com/renard_0)

License: WTFPL, grab your copy here: http://www.wtfpl.net
