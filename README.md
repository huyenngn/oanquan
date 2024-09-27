# Ô Ăn Quan

![Deploy](https://github.com/huyenngn/oanquan/actions/workflows/deploy.yml/badge.svg)
![License: MIT](https://img.shields.io/github/license/huyenngn/oanquan)

A Vietnamese traditional board game, Ô Ăn Quan, with an AI that uses the Minimax algorithm with Alpha-Beta pruning to play against human players.

To play the game, check it out at [oanquan.fun](https://oanquan.fun).

## Quick Start

You can host the API server and the frontend on your own machine.

Add the backend URLs to an `.env` file in the `frontend` directory (optional):

```sh
echo "VITE_BACKEND_NA={VITE_BACKEND_NA}" >> frontend/.env
echo "VITE_BACKEND_EU={VITE_BACKEND_EU}" >> frontend/.env
echo "VITE_BACKEND_AS={VITE_BACKEND_AS}" >> frontend/.env
```

Add your Supabase URL and key to the `.env` file in the `frontend` directory:

```sh
echo "VITE_SUPABASE_URL={SUPABASE_URL}" >> frontend/.env
echo "VITE_SUPABASE_KEY={SUPABASE_KEY}" >> frontend/.env
```

Build and run the app with Docker:

```sh
docker compose build
docker compose up
```

The API server will be running at `http://localhost:8080` and the frontend will be served at `http://localhost`.

## Development

To set up a development environment, clone the project and install it into a virtual environment.

```sh
git clone https://github.com/huyenngn/oanquan.git
cd oanquan
python -m venv .venv

source .venv/bin/activate

pip install -e .
```

To develop the frontend, use the following command:

```sh
cd frontend
npm install
npm run dev
```

To run the backend, use the following command:

```sh
python -m oanquan.api
```

The backend server will be running at `http://localhost:8080` and the live frontend will be served at `http://localhost:5173`.

## Features

-   [x] Play Ô ăn quan AI in easy mode
-   [x] Minimax algorithm with Alpha-Beta pruning for normal and hard mode
-   [x] Leaderboard
-   [ ] Send real game data to cloud for training and analysis
