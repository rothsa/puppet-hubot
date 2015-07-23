puppet-hubot
============
James Fryman <james@frymanet.com>

This module deploys [Hubot](https://hubot.github.com)

# Quick Start

[Install and bootstrap](https://hubot.github.com/docs/) a Hubot instance

Tested on Debian Squeeze and CentOS 6

# Requirements

Puppet Labs Standard Library
- http://github.com/puppetlabs/puppetlabs-stdlib

Puppet Labs NodeJS
- http://github.com/puppetlabs/puppetlabs-nodejs

<pre>
  class { 'hubot':
    adapter => 'irc',
    irc_nickname => 'crunchy',
    irc_server   => 'irc.freenode.com',
    irc_rooms    => ['#soggies'],
  }
</pre>

# Environment Variables
Some scripts require environment variables to be set at run time. this can be acheived with the environment option:

<pre>
  class { 'hubot':
    adapter => 'irc',
    irc_nickname => 'crunchy',
    irc_server   => 'irc.freenode.com',
    irc_rooms    => ['#soggies'],
    environment  => [ 'MYVAR=VAR1', 'THISVAR=that' ],
  }
</pre>

