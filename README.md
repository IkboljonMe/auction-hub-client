# Auction Hub Client

Frontend for **Auction Hub**, an online auction app. You can see all auctions, open one, watch the countdown and place bids. New bids show up for everyone right away without refreshing, thanks to Socket.IO. I built it to learn real-time features in React together with my own Node.js backend.

**Live:** https://client-auction-hub.vercel.app (the free server is often sleeping, so data may not load)

**Server repo:** [auction-hub-server](https://github.com/IkboljonMe/auction-hub-server)

## Features

- Sign up and sign in (JWT saved in the app state)
- List of all auctions
- Auction page with countdown timer, current bid and bid history
- Place a bid, the page updates live for all users
- Shows "You have the highest bid" and the winner when time is over
- Create auction with image upload (image upload is for admins)
- Admin can delete auctions
- Auction and create pages are only for logged in users

## Built with

- React 18 (Create React App)
- React Router v6
- Socket.IO client
- Axios
- Tailwind CSS
- React Toastify
- React Helmet Async
- Swiper

## How to run

Start the [server](https://github.com/IkboljonMe/auction-hub-server) first, then:

```bash
git clone https://github.com/IkboljonMe/auction-hub-client.git
cd auction-hub-client
npm install
cp .env.example .env
npm start
```

`.env` has one variable, the server address:

```
REACT_APP_API_PROXY=http://localhost:5000
```

The app opens on http://localhost:3000

To make a production build run `npm run build`.

## Project structure

```
src/
  App.jsx
  base/
    pages/        home, auction list, auction detail, create auction, login, register
    components/   auction card, loading, protected route
    routes/       all routes
    context/      global store (user info)
    styles/
```

---

Made by [IkboljonMe](https://github.com/IkboljonMe)
