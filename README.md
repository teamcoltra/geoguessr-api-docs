# GeoGuessr API Documentation

A comprehensive collection of GeoGuessr API endpoints with example responses. All API responses were fetched using authenticated requests with the `_ncfa` cookie.

## Table of Contents

- [Authentication](#authentication)
- [API Version 3 Endpoints](#api-version-3-endpoints)
  - [Account Management](#account-management)
  - [User Profiles & Stats](#user-profiles--stats)
  - [Games & Challenges](#games--challenges)
  - [Social Features](#social-features)
  - [Maps & Explorer](#maps--explorer)
  - [Subscriptions & Badges](#subscriptions--badges)
- [API Version 4 Endpoints](#api-version-4-endpoints)
  - [App State & System](#app-state--system)
  - [User Features](#user-features)
  - [Ranking System](#ranking-system)
  - [Game Modes](#game-modes)
  - [Seasonal Content](#seasonal-content)
- [Other Endpoints](#other-endpoints)
- [Usage Instructions](#usage-instructions)

## Authentication

All API endpoints require authentication using the `_ncfa` cookie. This cookie contains the session token needed to access user-specific data and protected endpoints.

## API Version 3 Endpoints

### Account Management

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `POST /api/v3/accounts/signin` | [`signin.json`](v3/geoguessr.com_api_v3_accounts_signin.json) | User sign-in |
| `POST /api/v3/accounts/signout` | [`signout.json`](v3/geoguessr.com_api_v3_accounts_signout.json) | User sign-out |

### User Profiles & Stats

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v3/profiles` | [`profiles.json`](v3/geoguessr.com_api_v3_profiles.json) | Current user profile |
| `GET /api/v3/profiles/stats` | [`profiles_stats.json`](v3/geoguessr.com_api_v3_profiles_stats.json) | Current user statistics |
| `GET /api/v3/profiles/wallet` | [`profiles_wallet.json`](v3/geoguessr.com_api_v3_profiles_wallet.json) | User wallet information |
| `GET /api/v3/profiles/maps` | [`profiles_maps.json`](v3/geoguessr.com_api_v3_profiles_maps.json) | User's created maps |
| `GET /api/v3/profiles/achievements` | [`achievements.json`](v3/geoguessr.com_api_v3_profiles_achievements.json) | User achievements |
| `GET /api/v3/users/<user-id>/stats` | [`user_stats.json`](v3/geoguessr.com_api_v3_users_user-id_stats.json) | Specific user statistics |

### Games & Challenges

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v3/games` | [`games.json`](v3/geoguessr.com_api_v3_games.json) | Game information |
| `GET /api/v3/games/<game-token>` | [`game_details.json`](v3/geoguessr.com_api_v3_games_game-token.json) | Specific game details |
| `GET /api/v3/games/streak` | [`streak.json`](v3/geoguessr.com_api_v3_games_streak.json) | Current streak information |
| `GET /api/v3/challenges/daily-challenges/today` | [`daily_today.json`](v3/geoguessr.com_api_v3_challenges_daily-challenges_today.json) | Today's daily challenge |
| `GET /api/v3/challenges/daily-challenges/tomorrow` | [`daily_tomorrow.json`](v3/geoguessr.com_api_v3_challenges_daily-challenges_tomorrow.json) | Tomorrow's daily challenge |
| `GET /api/v3/challenges/daily-challenges/previous` | [`daily_previous.json`](v3/geoguessr.com_api_v3_challenges_daily-challenges_previous.json) | Previous daily challenges |
| `GET /api/v3/challenges/daily-challenges/me/week` | [`daily_week.json`](v3/geoguessr.com_api_v3_challenges_daily-challenges_me_week.json) | User's weekly challenge progress |
| `GET /api/v3/competitions` | [`competitions.json`](v3/geoguessr.com_api_v3_competitions.json) | Available competitions |

### Social Features

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v3/social/friends` | [`friends.json`](v3/geoguessr.com_api_v3_social_friends.json) | User's friends list |
| `GET /api/v3/social/friends/received` | [`friends_received.json`](v3/geoguessr.com_api_v3_social_friends_received.json) | Received friend requests |
| `GET /api/v3/social/friends/summary` | [`friends_summary.json`](v3/geoguessr.com_api_v3_social_friends_summary.json) | Friends summary |
| `GET /api/v3/social/friendships` | [`friendships.json`](v3/geoguessr.com_api_v3_social_friendships.json) | Friendship relationships |
| `GET /api/v3/social/events/unfinishedgames` | [`unfinished_games.json`](v3/geoguessr.com_api_v3_social_events_unfinishedgames.json) | Unfinished multiplayer games |

### Maps & Explorer

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v3/explorer` | [`explorer.json`](v3/geoguessr.com_api_v3_explorer.json) | Explorer mode data |
| `GET /api/v3/explorer/medal-summary` | [`medal_summary.json`](v3/geoguessr.com_api_v3_explorer_medal-summary.json) | Explorer medal summary |
| `GET /api/v3/social/maps/browse/featured` | [`maps_featured.json`](v3/geoguessr.com_api_v3_social_maps_browse_featured.json) | Featured maps |
| `GET /api/v3/social/maps/browse/popular/all` | [`maps_popular_all.json`](v3/geoguessr.com_api_v3_social_maps_browse_popular_all.json) | All popular maps |
| `GET /api/v3/social/maps/browse/popular/official` | [`maps_popular_official.json`](v3/geoguessr.com_api_v3_social_maps_browse_popular_official.json) | Popular official maps |
| `GET /api/v3/social/maps/browse/popular/random` | [`maps_random.json`](v3/geoguessr.com_api_v3_social_maps_browse_popular_random.json) | Random popular maps |
| `GET /api/v3/social/maps/browse/personalized` | [`maps_personalized.json`](v3/geoguessr.com_api_v3_social_maps_browse_personalized.json) | Personalized map recommendations |
| `GET /api/v3/scores/maps` | [`scores_maps.json`](v3/geoguessr.com_api_v3_scores_maps.json) | Map scores |

### Subscriptions & Badges

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v3/subscriptions` | [`subscriptions.json`](v3/geoguessr.com_api_v3_subscriptions.json) | User subscriptions |
| `GET /api/v3/subscriptions/all` | [`subscriptions_all.json`](v3/geoguessr.com_api_v3_subscriptions_all.json) | All available subscriptions |
| `GET /api/v3/subscriptions/plans` | [`subscription_plans.json`](v3/geoguessr.com_api_v3_subscriptions_plans.json) | Available subscription plans |
| `GET /api/v3/subscriptions/elite/coins` | [`elite_coins.json`](v3/geoguessr.com_api_v3_subscriptions_elite_coins.json) | Elite subscription coins |
| `GET /api/v3/social/badges/unclaimed` | [`badges_unclaimed.json`](v3/geoguessr.com_api_v3_social_badges_unclaimed.json) | Unclaimed badges |
| `POST /api/v3/social/badges/claim` | [`badges_claim.json`](v3/geoguessr.com_api_v3_social_badges_claim.json) | Claim badges |

### Other V3 Endpoints

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v3/search/user` | [`search_user.json`](v3/geoguessr.com_api_v3_search_user.json) | User search |
| `GET /api/v3/likes` | [`likes.json`](v3/geoguessr.com_api_v3_likes.json) | User likes |
| `GET /api/v3/experiments` | [`experiments.json`](v3/geoguessr.com_api_v3_experiments.json) | A/B testing experiments |
| `POST /api/v3/analytics/impression` | [`analytics.json`](v3/geoguessr.com_api_v3_analytics_impression.json) | Analytics tracking |

## API Version 4 Endpoints

### App State & System

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v4/app/state` | [`app_state.json`](v4/geoguessr.com_api_v4_app_state.json) | Application state |
| `GET /api/v4/announcements` | [`announcements.json`](v4/geoguessr.com_api_v4_announcements.json) | System announcements |
| `GET /api/v4/activities` | [`activities.json`](v4/geoguessr.com_api_v4_activities.json) | User activities |
| `GET /api/v4/notifications` | [`notifications.json`](v4/geoguessr.com_api_v4_notifications.json) | User notifications |
| `GET /api/v4/chat/emotes` | [`chat_emotes.json`](v4/geoguessr.com_api_v4_chat_emotes.json) | Available chat emotes |

### User Features

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v4/avatar/user/<user-id>` | [`avatar_user.json`](v4/geoguessr.com_api_v4_avatar_user_user-id.json) | User avatar data |
| `GET /api/v4/stats/me` | [`stats_me.json`](v4/geoguessr.com_api_v4_stats_me.json) | Current user statistics |
| `GET /api/v4/feed/friends` | [`feed_friends.json`](v4/geoguessr.com_api_v4_feed_friends.json) | Friends activity feed |
| `GET /api/v4/feed/private` | [`feed_private.json`](v4/geoguessr.com_api_v4_feed_private.json) | Private activity feed |
| `GET /api/v4/parties` | [`parties.json`](v4/geoguessr.com_api_v4_parties.json) | Party information |
| `GET /api/v4/search/map` | [`search_map.json`](v4/geoguessr.com_api_v4_search_map.json) | Map search |

### Ranking System

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v4/ranked-system/divisions` | [`ranked_divisions.json`](v4/geoguessr.com_api_v4_ranked-system_divisions.json) | Ranking system divisions |
| `GET /api/v4/ranked-system/me` | [`ranked_me.json`](v4/geoguessr.com_api_v4_ranked-system_me.json) | Current user ranking |
| `GET /api/v4/ranked-system/me/weeks` | [`ranked_weeks.json`](v4/geoguessr.com_api_v4_ranked-system_me_weeks.json) | User's weekly ranking history |
| `GET /api/v4/ranked-system/best/<user-id>` | [`ranked_best.json`](v4/geoguessr.com_api_v4_ranked-system_best_user-id.json) | User's best ranking |
| `GET /api/v4/ranked-system/progress/<user-id>` | [`ranked_progress.json`](v4/geoguessr.com_api_v4_ranked-system_progress_user-id.json) | User ranking progress |
| `GET /api/v4/ranked-team-duels/best/<user-id>` | [`team_duels_best.json`](v4/geoguessr.com_api_v4_ranked-team-duels_best_user-id.json) | Best team duels performance |

### Game Modes

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v4/games/infinity` | [`games_infinity.json`](v4/geoguessr.com_api_v4_games_infinity.json) | Infinity game mode |
| `GET /api/v4/globetrotter/trip/current` | [`globetrotter_current.json`](v4/geoguessr.com_api_v4_globetrotter_trip_current.json) | Current globetrotter trip |
| `GET /api/v4/globetrotter/locations` | [`globetrotter_locations.json`](v4/geoguessr.com_api_v4_globetrotter_locations.json) | Globetrotter locations |
| `GET /api/v4/globetrotter/location/<location-id>` | [`globetrotter_location.json`](v4/geoguessr.com_api_v4_globetrotter_location_location-id.json) | Specific globetrotter location |

### Seasonal Content

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v4/seasons/active/stats` | [`seasons_active.json`](v4/geoguessr.com_api_v4_seasons_active_stats.json) | Active season statistics |
| `GET /api/v4/seasons/previous` | [`seasons_previous.json`](v4/geoguessr.com_api_v4_seasons_previous.json) | Previous seasons |
| `GET /api/v4/seasons/next` | [`seasons_next.json`](v4/geoguessr.com_api_v4_seasons_next.json) | Upcoming seasons |
| `GET /api/v4/seasons/game/BattleRoyaleCountries` | [`battle_royale.json`](v4/geoguessr.com_api_v4_seasons_game_BattleRoyaleCountries.json) | Battle Royale Countries season |

### Missions & Objectives

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/v4/missions` | [`missions.json`](v4/geoguessr.com_api_v4_missions.json) | Available missions |
| `GET /api/v4/objectives` | [`objectives.json`](v4/geoguessr.com_api_v4_objectives.json) | User objectives |
| `GET /api/v4/objectives/unclaimed` | [`objectives_unclaimed.json`](v4/geoguessr.com_api_v4_objectives_unclaimed.json) | Unclaimed objectives |
| `GET /api/v4/webshop/daily-shop-claim` | [`daily_shop.json`](v4/geoguessr.com_api_v4_webshop_daily-shop-claim.json) | Daily shop claims |

## Other Endpoints

| Endpoint | Sample File | Description |
|----------|-------------|-------------|
| `GET /api/maps?createdBy=<user-id>&page=0&count=200` | [`user_maps.json`](other/geoguessr.com_api_maps_createdBy=user-id_page=0_count=200.json) | Maps created by user |
| `GET /duels/<game-id>/summary` | [`duel_summary.json`](other/geoguessr.com_duels_game-id_summary.json) | Duel game summary |
| `GET /_next/data/.../en/multiplayer.json` | [`next_multiplayer.json`](other/geoguessr.com__next_data_tUo_uqfjUYj8EDtv81xrR_en_multiplayer.json.json) | Next.js multiplayer data |
| `GET /_next/data/.../en/streaks.json` | [`next_streaks.json`](other/geoguessr.com__next_data_tUo_uqfjUYj8EDtv81xrR_en_streaks.json.json) | Next.js streaks data |
| `GET /_next/data/.../en/user/<user-id>.json` | [`next_user.json`](other/geoguessr.com__next_data_tUo_uqfjUYj8EDtv81xrR_en_user_user-id.json_slug=user-id.json) | Next.js user data |

## Usage Instructions

1. **Authentication**: Ensure you have a valid `_ncfa` cookie from an authenticated GeoGuessr session
2. **Rate Limiting**: Be respectful with API calls to avoid being rate-limited
3. **Placeholders**: URLs containing `<user-id>`, `<game-token>`, etc. should be replaced with actual values
4. **Response Format**: All endpoints return JSON responses

## Notes

- All sample responses are stored in their respective version directories (`v3/`, `v4/`, `other/`)
- Some endpoints may require additional parameters or specific HTTP methods (GET/POST)
- Response structures may change as GeoGuessr updates their API
- This documentation is based on reverse engineering and may not be complete or officially supported
