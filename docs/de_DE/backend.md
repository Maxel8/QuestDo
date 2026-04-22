# Backend

## Architecture

```mermaid
graph TD
User --> Frontend
Frontend --> login_query
Frontend --> user_quest_query
Frontend --> quest_query

login_query --> api_login
user_quest_query --> api_user_quest
quest_query --> api_quest

api_login["/api/login"] --> user_db
api_user_quest["/api/user/{user_id}/quest"] --> user_db
api_quest["/api/quest/{quest_id}"] --> quests_db
