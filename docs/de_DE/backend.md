# Backend

## Architecture

```mermaid
graph TD
User --> Frontend
Frontend --> login_query
Frontend --> user_quest_query
Frontend --> quest_query
login_query --> api/login
user_quest_query --> api/user/[user_id]/quest
quest_query --> api/quest/[quest_id]
api/login --> user.db
api/user/[user_id]/quest --> user.db
api/quest/[quest_id] --> quests.db