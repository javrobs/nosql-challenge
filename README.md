# Mongo Challenge
# Introduction
This challenge was divided in two sections:
- For the first part, we had to import a Mongo Database, create a new document in a collection, update it and then delete a few documents according to queries.
- In the second part, we used mongo queries to respond to several questions.
# Questions and analysis
1. Which establishments have a hygiene score equal to 20?
    - Count: There are 41 establishments with a hygiene score of 20.
    - find_one() results:
    ````
    {'AddressLine1': '5-6 Southfields Road',
    'AddressLine2': 'Eastbourne',
    'AddressLine3': 'East Sussex',
    'AddressLine4': '',
    'BusinessName': 'The Chase Rest Home',
    'BusinessType': 'Caring Premises',
    'BusinessTypeID': 5,
    'ChangesByServerID': 0,
    'Distance': 4613.888288172291,
    'FHRSID': 110681,
    'LocalAuthorityBusinessID': '4029',
    'LocalAuthorityCode': '102',
    'LocalAuthorityEmailAddress': 'Customerfirst@eastbourne.gov.uk',
    'LocalAuthorityName': 'Eastbourne',
    'LocalAuthorityWebSite': 'http://www.eastbourne.gov.uk/foodratings',
    'NewRatingPending': False,
    'Phone': '',
    'PostCode': 'BN21 1BU',
    'RatingDate': '2021-09-23T00:00:00',
    'RatingKey': 'fhrs_0_en-gb',
    'RatingValue': '0',
    'RightToReply': '',
    'SchemeType': 'FHRS',
    '_id': ObjectId('6444b1b007071076e94c543b'),
    'geocode': {'latitude': 50.769705, 'longitude': 0.27694},
    'links': [{'href': 'https://api.ratings.food.gov.uk/establishments/110681',
                'rel': 'self'}],
    'meta': {'dataSource': None,
            'extractDate': '0001-01-01T00:00:00',
            'itemCount': 0,
            'pageNumber': 0,
            'pageSize': 0,
            'returncode': None,
            'totalCount': 0,
            'totalPages': 0},
    'scores': {'ConfidenceInManagement': 20, 'Hygiene': 20, 'Structural': 20}}
    ````
2. Which establishments in London have a RatingValue greater than or equal to 4?
    - Count: There are 33 establishments in London with a 4 or greater rating.
    - find_one() results:
    ````
    {'AddressLine1': 'Oak Apple Farm Building 103 Sheernes Docks',
    'AddressLine2': 'Sheppy Kent',
    'AddressLine3': '',
    'AddressLine4': '',
    'BusinessName': "Charlie's",
    'BusinessType': 'Other catering premises',
    'BusinessTypeID': 7841,
    'ChangesByServerID': 0,
    'Distance': 4627.439467780196,
    'FHRSID': 621707,
    'LocalAuthorityBusinessID': 'PI/000025307',
    'LocalAuthorityCode': '508',
    'LocalAuthorityEmailAddress': 'publicprotection@cityoflondon.gov.uk',
    'LocalAuthorityName': 'City of London Corporation',
    'LocalAuthorityWebSite': 'http://www.cityoflondon.gov.uk/Corporation/homepage.htm',
    'NewRatingPending': False,
    'Phone': '',
    'PostCode': 'ME12',
    'RatingDate': '2021-10-18T00:00:00',
    'RatingKey': 'fhrs_4_en-gb',
    'RatingValue': 4.0,
    'RightToReply': '',
    'SchemeType': 'FHRS',
    '_id': ObjectId('644621d802a0a6627ab4eabb'),
    'geocode': {'latitude': 51.369321, 'longitude': 0.508551},
    'links': [{'href': 'https://api.ratings.food.gov.uk/establishments/621707',
                'rel': 'self'}],
    'meta': {'dataSource': None,
            'extractDate': '0001-01-01T00:00:00',
            'itemCount': 0,
            'pageNumber': 0,
            'pageSize': 0,
            'returncode': None,
            'totalCount': 0,
            'totalPages': 0},
    'scores': {'ConfidenceInManagement': 5, 'Hygiene': 5, 'Structural': 10}}
    ````
3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
    - Count: There are 33 establishments in London with a 4 or greater rating.
    - find_one() results:
    ````
    {'AddressLine1': '130 - 132 Plumstead High Street',
    'AddressLine2': '',
    'AddressLine3': 'Plumstead',
    'AddressLine4': 'Greenwich',
    'BusinessName': 'Volunteer',
    'BusinessType': 'Pub/bar/nightclub',
    'BusinessTypeID': 7843,
    'ChangesByServerID': 0,
    'Distance': 4646.965634598608,
    'FHRSID': 694609,
    'LocalAuthorityBusinessID': 'PI/000116619',
    'LocalAuthorityCode': '511',
    'LocalAuthorityEmailAddress': 'health@royalgreenwich.gov.uk',
    'LocalAuthorityName': 'Greenwich',
    'LocalAuthorityWebSite': 'http://www.royalgreenwich.gov.uk',
    'NewRatingPending': False,
    'Phone': '',
    'PostCode': 'SE18 1JQ',
    'RatingDate': '2019-08-05T00:00:00',
    'RatingKey': 'fhrs_5_en-gb',
    'RatingValue': 5.0,
    'RightToReply': '',
    'SchemeType': 'FHRS',
    '_id': ObjectId('644621d902a0a6627ab528fb'),
    'geocode': {'latitude': 51.4873437, 'longitude': 0.09208},
    'links': [{'href': 'http://api.ratings.food.gov.uk/establishments/694609',
                'rel': 'self'}],
    'meta': {'dataSource': None,
            'extractDate': '0001-01-01T00:00:00',
            'itemCount': 0,
            'pageNumber': 0,
            'pageSize': 0,
            'returncode': None,
            'totalCount': 0,
            'totalPages': 0},
    'scores': {'ConfidenceInManagement': 0, 'Hygiene': 0, 'Structural': 0}}
    ````

4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.
    - First ten authority areas:
    ````
    {'_id': 'Thanet', 'count': 1130}
    {'_id': 'Greenwich', 'count': 882}
    {'_id': 'Maidstone', 'count': 713}
    {'_id': 'Newham', 'count': 711}
    {'_id': 'Swale', 'count': 686}
    {'_id': 'Chelmsford', 'count': 680}
    {'_id': 'Medway', 'count': 672}
    {'_id': 'Bexley', 'count': 607}
    {'_id': 'Southend-On-Sea', 'count': 586}
    {'_id': 'Tendring', 'count': 542}
    ````