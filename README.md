# Create the application
https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/apps/addApp
<details>
<summary>request</summary>
  
```
curl -X 'POST' \
  'https://virtserver.swaggerhub.com/artalex/ConsoleCI/1.0.0/apps' \
  -H 'APY-KEY: private-developer-api-key'
```
</details>
<details>
  <summary>response</summary>
  
```json
{
  "id": 1
}
```
</details>

# Create the draft
https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/apps/createDraft

Category IDs can be obtained using the method https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/misc/getCategories
Tag IDs can be obtained using the method https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/misc/getTags
<details>
<summary>request</summary>
  
```
curl -X 'POST' \
  'https://virtserver.swaggerhub.com/artalex/ConsoleCI/1.0.0/apps/1/draft' \
  -H 'APY-KEY: private-developer-api-key' \
  -H 'Content-Type: application/json' \
  -d '{
  "age-rating": "18+",
  "apple-team-id": "7E25NJES4E",
  "categories": [
    1,
    2
  ],
  "description": {
    "en": "My First Game"
  },
  "instruction": {
    "en": "Enjoy the Game!!!"
  },
  "keywords": [
    "super",
    "cool"
  ],
  "languages": [
    "en"
  ],
  "open-economy": false,
  "optimized-for": {
    "mobile": true,
    "desktop": true
  },
  "orientation": "landscape",
  "platforms": {
    "ios": {
      "other": true
    },
    "android": {
      "other": true
    },
    "desktop": {
      "other": true
    }
  },
  "seo-description": {
    "en": "absolutely free"
  },
  "tags": [
    1,
    2,
    3
  ],
  "title": {
    "en": "Super Game #1",
  },
  "user-data-required": true,
  "version": "1.0.0.0",
}'
```
</details>
<details>
<summary>response</summary>
  
```json
{
  "age-rating": "18+",
  "apple-team-id": "7E25NJES4E",
  "categories": [
    1,
    2
  ],
  "cover": {
  },
  "description": {
    "en": "My First Game"
  },
  "icon": {
  },
  "instruction": {
    "en": "Enjoy the Game!!!"
  },
  "keywords": [
    "super",
    "cool"
  ],
  "languages": [
    "en"
  ],
  "open-economy": false,
  "optimized-for": {
    "mobile": true,
    "desktop": true
  },
  "orientation": "landscape",
  "platforms": {
    "ios": {
      "other": true
    },
    "android": {
      "other": true
    },
    "desktop": {
      "other": true
    }
  },
  "screenshots": {
    "common": [
    ],
    "mobile": [
    ],
    "desktop": [
    ]
  },
  "seo-description": {
    "en": "absolutely free",
  },
  "tags": [
    1,
    2,
    3
  ],
  "title": {
    "en": "Super Game #1"
  },
  "user-data-required": true,
  "version": "1.0.0.0",
  "videos": {
    "common": [
    ],
    "mobile": [
    ],
    "desktop": [
    ]
  }
}
```
</details>

# Load the media files
Requirements for media files can be found here https://yandex.ru/dev/games/doc/dg/console/add-new-game.html?lang=en
## Load the icon
https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/files/uploadImage
<details>
<summary>request</summary>
  
```
curl -X 'POST' \
  'https://virtserver.swaggerhub.com/artalex/ConsoleCI/1.0.0/apps/1/uploadImage' \
  -H 'APY-KEY: private-developer-api-key' \
  -H 'Content-Type: application/octet-stream' \
  --data-binary @icon.png
```
</details>
<details>
<summary>response</summary>
  
```json
{
  "id": 1,
  "prefix-url": "https://prefix.url/1",
  "timestamp": 1635494567
}
```
</details>

## Load the cover
https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/files/uploadImage
<details>
<summary>request</summary>
  
```
curl -X 'POST' \
  'https://virtserver.swaggerhub.com/artalex/ConsoleCI/1.0.0/apps/1/uploadImage' \
  -H 'APY-KEY: private-developer-api-key' \
  -H 'Content-Type: application/octet-stream' \
  --data-binary @cover.png
```
</details>
<details>
<summary>response</summary>
  
```json
{
  "id": 2,
  "prefix-url": "https://prefix.url/2",
  "timestamp": 1635494567
}
```
</details>

## Load the screenshot
https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/files/uploadImage
<details>
<summary>request</summary>
  
```
curl -X 'POST' \
  'https://virtserver.swaggerhub.com/artalex/ConsoleCI/1.0.0/apps/1/uploadImage' \
  -H 'APY-KEY: private-developer-api-key' \
  -H 'Content-Type: application/octet-stream' \
  --data-binary @screenshot.png
```
</details>
<details>
<summary>response</summary>
  
```json
{
  "id": 3,
  "prefix-url": "https://prefix.url/3",
  "timestamp": 1635494567
}
```
</details>

## Load the video
https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/files/uploadVideo
<details>
<summary>request</summary>
  
```
curl -X 'POST' \
  'https://virtserver.swaggerhub.com/artalex/ConsoleCI/1.0.0/apps/1/uploadVideo' \
  -H 'APY-KEY: private-developer-api-key' \
  -H 'Content-Type: application/octet-stream' \
  --data-binary @video.mp4
```
</details>
<details>
<summary>response</summary>
  
```json
{
  "id": 1,
  "timestamp": 1635494567,
  "status": "processing"
}
```
</details>

## Edit the draft
https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/apps/changeDraft

When editing, you can specify any non-empty set of fields - only those fields that will be presented in the set will be changed.
However, each field must be specified in its entirety: that is, if a Russian name is added (field ##title##), then both the existing value (key ##en##) and the new one must be specified

```json
{
  "title": {
    "en": "Super Game #1",
    "ru": "Супер-игра №1"
  }
}
```

<details>
<summary>request</summary>
  
```
curl -X 'PATCH' \
  'https://virtserver.swaggerhub.com/artalex/ConsoleCI/1.0.0/apps/1/draft' \
  -H 'APY-KEY: private-developer-api-key' \
  -H 'Content-Type: application/json' \
  -d '{
  "cover": {
    "en": {
      "id": 1
    }
  },
  "icon": {
    "en": {
      "id": 2
    }
  },
  "screenshots": {
    "common": [
      {
        "en": {
          "id": 3
        }
      }
    ],
    "mobile": [
    ],
    "desktop": [
    ]
  },
  "videos": {
    "common": [
      {
        "en": {
          "id": 1
        }
      }
    ]
  }
}'
```
</details>
<details>
<summary>response</summary>
  
```json
{
  "age-rating": "18+",
  "apple-team-id": "7E25NJES4E",
  "categories": [
    1,
    2
  ],
  "cover": {
    "en": {
      "id": 1
    }
  },
  "description": {
    "en": "My First Game"
  },
  "icon": {
    "en": {
      "id": 2
    }
  },
  "instruction": {
    "en": "Enjoy the Game!!!"
  },
  "keywords": [
    "super",
    "cool"
  ],
  "languages": [
    "en"
  ],
  "open-economy": false,
  "optimized-for": {
    "mobile": true,
    "desktop": true
  },
  "orientation": "landscape",
  "platforms": {
    "ios": {
      "other": true
    },
    "android": {
      "other": true
    },
    "desktop": {
      "other": true
    }
  },
  "screenshots": {
    "common": [
      {
        "en": {
          "id": 3
        }
      }
    ],
    "mobile": [
    ],
    "desktop": [
    ]
  },
  "seo-description": {
    "en": "absolutely free",
  },
  "tags": [
    1,
    2,
    3
  ],
  "title": {
    "en": "Super Game #1"
  },
  "user-data-required": true,
  "version": "1.0.0.0",
  "videos": {
    "common": [
      {
        "en": {
          "id": 1
        }
      }
    ]
  }
}
```
</details>

# Load the application archive
Requirements for archive can be found here https://yandex.ru/dev/games/doc/dg/console/add-new-game.html?lang=en
## Load the archive
https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/files/uploadSources
<details>
<summary>request</summary>
  
```
curl -X 'POST' \
  'https://virtserver.swaggerhub.com/artalex/ConsoleCI/1.0.0/apps/1/uploadSources' \
  -H 'APY-KEY: private-developer-api-key' \
  -H 'Content-Type: application/octet-stream' \
  --data-binary @sources.zip
```
</details>
<details>
<summary>response</summary>
  
```json
{
  "id": 1,
  "timestamp": 1635494567,
  "status": "processing"
}
```
</details>

## Edit the draft
https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/apps/changeDraft
<details>
<summary>request</summary>
  
```
curl -X 'PATCH' \
  'https://virtserver.swaggerhub.com/artalex/ConsoleCI/1.0.0/apps/1/draft' \
  -H 'APY-KEY: private-developer-api-key' \
  -H 'Content-Type: application/json' \
  -d '{
  "source-file": 1
  }'
```
</details>
<details>
<summary>response</summary>
  
```json
{
  "age-rating": "18+",
  "apple-team-id": "7E25NJES4E",
  "categories": [
    1,
    2
  ],
  "cover": {
    "en": {
      "id": 1
    }
  },
  "description": {
    "en": "My First Game"
  },
  "icon": {
    "en": {
      "id": 2
    }
  },
  "instruction": {
    "en": "Enjoy the Game!!!"
  },
  "keywords": [
    "super",
    "cool"
  ],
  "languages": [
    "en"
  ],
  "open-economy": false,
  "optimized-for": {
    "mobile": true,
    "desktop": true
  },
  "orientation": "landscape",
  "platforms": {
    "ios": {
      "other": true
    },
    "android": {
      "other": true
    },
    "desktop": {
      "other": true
    }
  },
  "screenshots": {
    "common": [
      {
        "en": {
          "id": 3
        }
      }
    ],
    "mobile": [
    ],
    "desktop": [
    ]
  },
  "seo-description": {
    "en": "absolutely free",
  },
  "sources-file": 1,
  "tags": [
    1,
    2,
    3
  ],
  "title": {
    "en": "Super Game #1"
  },
  "user-data-required": true,
  "version": "1.0.0.0",
  "videos": {
    "common": [
      {
        "en": {
          "id": 1
        }
      }
    ]
  }
}
```
</details>

# Submit the application for moderation
Requirements for the game can be seen here  https://yandex.ru/dev/games/doc/dg/concepts/requirements.html?lang=en#requirements
## Submit the application
https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/apps/startModeration
<details>
<summary>request</summary>
  
```
curl -X 'POST' \
  'https://virtserver.swaggerhub.com/artalex/ConsoleCI/1.0.0/apps/1/moderation/start' \
  -H 'APY-KEY: private-developer-api-key'
```
</details>
<details>
<summary>response</summary>
  
```json
{
  "status": "idle"
}
```
</details>

## Check status
https://app.swaggerhub.com/apis-docs/artalex/ConsoleCI/1.0.0#/apps/getModerationStatus
<details>
<summary>request</summary>
  
```
curl -X 'GET' \
  'https://virtserver.swaggerhub.com/artalex/ConsoleCI/1.0.0/apps/1/moderation/status' \
  -H 'APY-KEY: private-developer-api-key'
```
</details>
<details>
<summary>response</summary>
  
```json
{
  "status": "completed"
}
```
</details>
