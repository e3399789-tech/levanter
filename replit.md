# Levanter WhatsApp Bot

## Overview
This project is a wrapper/installer for the [Levanter WhatsApp Bot](https://github.com/lyfe00011/levanter). The root `index.js` handles:
- Cloning the `levanter/` repository (if not present)
- Installing dependencies via `yarn`
- Starting the bot using PM2, with a fallback to `node index.js`

## Project Layout
- `index.js` - Bootstrap/wrapper script
- `levanter/` - The actual Levanter bot (cloned from GitHub)
- `levanter/config.env` - Bot configuration (SESSION_ID, VPS flag)
- `levanter/config.env.example` - Example config

## Configuration
Edit `levanter/config.env` to set:
- `SESSION_ID` - Your WhatsApp session ID from the Levanter pairing process
- `VPS=true` - Marks this as a VPS deployment

## Running
The workflow runs `node index.js` which manages the lifecycle of the bot.

## Stack
- Node.js 20
- Yarn 1.22.22
- PM2 for process management
- Baileys (WhatsApp Web API)
