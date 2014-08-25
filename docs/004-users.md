# Group Users
Manage your user account.

## Users [/users]

### Retrieve all Users [GET]
Returns a list of users that the are accessible to the current user (all users
in the current user's organizations, essentially).

+ Response 200

    + Body

            {
                "users": [
                    { 'href': 'https://api.packethost.net/users/3D987365-E24A-48F9-875B-15919526AE5A' },
                    { 'href': 'https://api.packethost.net/users/0488E769-4138-4940-9687-31D10305B685' },
                    { 'href': 'https://api.packethost.net/users/B2403E40-9329-436B-B782-591885451ABE' }
                ]
            }

## User [/users/{id}]

+ Model

        {
            "id": "333F576A-1F5F-4983-BAF1-89B0869FE704",
            "email": "example@example.com",
            "first_name": "Melissa",
            "last_name": "Smith",
            "full_name": "Melissa Smith",
            "timezone": "America/New_York",
            "twitter": "@melissasmith",
            "facebook": "https://facebook.com/melissa.smith",
            "linkedin": "melissasmith",
            "organizations": [
                { 'href': 'https://api.packethost.net/organizations/3D987365-E24A-48F9-875B-15919526AE5A' },
                { 'href': 'https://api.packethost.net/organizations/0488E769-4138-4940-9687-31D10305B685' }
            ],
            "memberships": [
                { 'href': 'https://api.packethost.net/memberships/3BE09DC2-5030-440B-B81A-AF7097B86F16' },
                { 'href': 'https://api.packethost.net/memberships/B2403E40-9329-436B-B782-591885451ABE' }
            ],
            "ssh-keys": [
                { 'href': 'https://api.packethost.net/ssh-keys/E343F687-CB0E-4EFF-A80A-73602AFAB1DF' }
            ],
            "created_at": "2014-04-14T02:15:15Z",
        }

### Retrieve a User [GET]

+ Response 200

    [User][]

## Current User [/user]
The currently logged-in user.

### Retrieve the Current User [GET]
Returns the user object for the currently logged-in user.

+ Response 200

    [User][]

### Update the Current User [PATCH]
Updates the currently logged-in user.

+ Response 204