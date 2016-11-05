#HSLIDE
# Git Pitch Test
This is a git pitch to test it's functionality as the concept seems fun and maybe practicable

#HSLIDE
# Some Code slides
See below

#VSLIDE

```Java
JSONObject broker = JsonReader.readFile(cf).getJSONObject("broker");
		JSONObject topics = broker.getJSONObject("topics");
		Database db = null;
		try {
			JSONObject database = JsonReader.readFile(cf).getJSONObject(
					"database");
			db = new Database(database.getString("dbHost"),
					database.getString("dbPort"), database.getString("dbName"),
					database.getString("dbUser"), database.getString("dbPass"));
		} catch (JSONException e) {
			System.err.println("No database mentioned in config file");
		}
		List<ClientMqtt> clients = new ArrayList<ClientMqtt>();
		List<Thread> clientThreads = new ArrayList<Thread>();
```

#VSLIDE

Config.json from my [mqtt-client](https://github.com/hadesrofl/mqtt-client) repo.
```
{
    "broker": {
        "address": "localhost",
        "port": "1883",
        "topics": {
            "t1": "temperature/living-room",
            "t2": "humidity/living-room"
        },
        "subscribe": "true" },
    "database":{
        "dbHost": "localhost",
        "dbPort": "3306",
        "dbName": "TableName",
        "dbUser": "Username",
        "dbPass": "Password"
    }
}
```

#HSLIDE
# The End
![Image-Relative](https://media.giphy.com/media/kOnoObmFUE0k8/giphy.gif)
