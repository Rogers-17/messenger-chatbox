# ODC Project -- Vue.js Chatbot Landing Page

A modern responsive landing page for a chatbot using VUE with a floating chatbot icon 

## Features

- **Facebook Messenger Integration**: Floating chat widget powered by Facebook Messenger
- **Responsive Design**: Beautiful UI that works on all devices

## Quick Start

- Clone the repository
- Install all dependencies
- Run the application

```bash
git clone https://github.com/messenger-chatbot-vue
npm install
npm run dev
```

Visit `http://localhost:5173` to see the application.


## Project Structure

```
src/
├── assets/
|      UI/UX/                   # The designs for the landing page
│      Images/                  # for any image we want to display
├── components/
│   ├── Navbar.vue              # Hero section with CTA
│   ├── Hero.vue                # Hero section with CTA
│   ├── Features.vue            # Feature highlights
│   ├── FAQs.vue                # Interactive FAQ accordion
│   ├── Footer.vue              # Footer with links
│   └── MessengerChat.vue       # Facebook Messenger plugin
├── App.vue                     # Main component where all the components will be displayed
├── main.js                     # Entry point
└── main.css                    # Global styles
```

## Collaboration

- **Commit Messages**
Examples:
``
git commit -m "Added Navbar"
git commit -m "Added Footer"

``