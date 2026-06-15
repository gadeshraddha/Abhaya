# Abhaya – Women Safety & Emergency Alert System

Abhaya is a project I'm building to make it easier for someone to send out an emergency alert and share their live location with trusted contacts, without having to dig through menus when they're already stressed or scared.

**Status:** early prototype / planning stage. This README describes the idea and what I'm aiming to build — implementation details will come together as the project progresses.

## Why I'm building this

Most safety apps look fine on paper but fall apart in an actual emergency — too many taps, confusing UI, or they don't communicate location clearly to whoever's supposed to help. The idea here is to strip it down to the basics: one button, your location gets shared instantly, and your emergency contacts get notified automatically.

## What it's meant to do

This is a software-only project for now — no hardware or wearable component. The core idea:

- A simple panic button that's quick to access
- Live location sharing so contacts know exactly where you are
- Emergency contacts who get notified automatically when the button is pressed
- A basic log/dashboard so you can see past alerts

Hardware integration (wearables, dedicated devices, etc.) might be something to explore down the line, but that's not the focus right now.

## Planned features

- **Panic button** – one tap to trigger an alert, with some protection against accidental presses
- **Live location** – shares current location with contacts when the alert goes out
- **Alerts** – notifies saved emergency contacts that the user needs help, along with their location
- **Contacts** – ability to add, edit, and remove emergency contacts
- **Dashboard** – view a history of past alerts
- **Low-key UI** – stays minimal during normal use so the panic button doesn't draw attention, but is still fast to reach

## How it's supposed to work

1. User opens the app
2. Taps the panic button
3. App captures the user's location
4. Sends an alert with that location to saved contacts
5. Logs the event
6. Confirms to the user that the alert went out

## Future ideas

- A proper mobile app
- Wearable/IoT integration
- Smarter detection (e.g. recognizing distress automatically)
- Voice-activated trigger

## Note

This is a learning/prototype project, not a production-ready safety tool — don't rely on it as your only safety measure.
