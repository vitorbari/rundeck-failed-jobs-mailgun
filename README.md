# rundeck_failed_jobs

[![Build Status](https://travis-ci.org/vitorbari/rundeck-failed-jobs.svg)](https://travis-ci.org/vitorbari/rundeck-failed-jobs)

A tool that user Rundeck API to get failed jobs information and sends it via email using Mandrill API.

## Installation

Download source via:

```
$ git clone https://github.com/vitorbari/rundeck-failed-jobs.git
```

You will need Go installed to build from source.

```
$ go build rundeck-failed-jobs.go
```

## Configuration

Open `conf.json`. 

You should specify your RunDeck server, Mandrill Key and recipients for the notifications.


## Usage

```
$ ./rundeck-failed-jobs --project=<project name> [--group<group name>] [--recentfilter=<filter>]
```

## Details

For more information about RunDeck API, go to <http://rundeck.org/2.6.0/api/index.html>.

Mandrill website <https://mandrillapp.com>.