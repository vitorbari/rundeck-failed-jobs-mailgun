# rundeck-failed-jobs-mailgun

[![Build Status](https://travis-ci.org/vitorbari/rundeck-failed-jobs-mailgun.svg)](https://travis-ci.org/vitorbari/rundeck-failed-jobs-mailgun)

A tool that uses Rundeck API to get failed jobs information and sends it via email using **Mailgun API**.

## Installation

Download source via:

```
$ git clone https://github.com/vitorbari/rundeck-failed-jobs-mailgun.git
```

You will need Go installed to build from source.

```
$ go build rundeck-failed-jobs-mailgun.go
```

## Configuration

Open `conf.json`. 

You should specify your RunDeck server, Mailgun Domains, Mailgun Keys and recipients for the notifications.


## Usage

```
$ ./rundeck-failed-jobs-mailgun --project=<project name> [--group<group name>] [--recentfilter=<filter>]
```

## Notification Example

Title: `[RunDeck] [ACME] 2 failures!`

Email Body:
```
2 Failed Executions from project [ACME].

Executions:
	ACME_SRV-APP05_PRD_UPDATE_STATUS
		http://192.168.0.10:4440/execution/follow/175085
		Started: 2015-12-06T18:00:00Z | User:vitor.bari
		Nodes: srv-app05

	ACME_SRV-APP05_PRD_CLEAR_LOGS
		http://192.168.0.10:4440/execution/follow/175079
		Started: 2015-12-06T17:55:00Z | User:vitor.bari
		Nodes: srv-app05
```

## Details

For more information about RunDeck API, go to <http://rundeck.org/2.6.0/api/index.html>.

Mailgun website <https://mailgun.com/>.