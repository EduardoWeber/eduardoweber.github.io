---
title: "GoTwitch"
date: 2022-10-16T12:00:38-03:00
draft: false
tags: ["go", "twitch", "random", "api", "vue", "javascript", "typescript", "web"]
categories: ["GoTwitch"]
---

[GoTwitch](https://gotwitch.efw.rocks/) is a random Twitch streamer picker. It's a simple web app that allows you to pick a random streamer using a set of filters. It's built with Go and Vue.js.

Access the app at [https://gotwitch.efw.rocks/](https://gotwitch.efw.rocks/).

## Premise

There are a lot of Twitch streamers out there, and it's hard to find a good one to watch. GoTwitch allows you to pick a random streamer using a set of filters matching your criteria. The app also allows you to save your filters for later use.

## Features

- Pick a random streamer
- Filter by game
- Filter by language
- Save filters on local storage

## How it works

The frontend is a single page application in Vue.js that communicates with the backend using a REST API. 

The backend has jobs that run on a schedule to update the database with the latest data from the Twitch API. The data is stored in a PostgreSQL database. When the user requests a random streamer, the backend queries the database applying the filters and returns the result to the frontend. We also have a job that keeps the categories up to date.

## Technologies

### Frontend

- Vue.js
- Vuetify 3 Beta (Material Design)
- TypeScript

### Backend

- Go (with Gin and GORM)
- Docker
- PostgreSQL