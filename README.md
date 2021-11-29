## Wealth Observer API
The public API that users could use to fetch data from our server. The https://wealthobserver.gr app is using the same api. The requests and their responses are described below:

### Request about politicians
Users can fetch all politicians by using the following request:
`https://api.wealthobserver.gr/politicians?_limit=-1`

An example response is like the following example:

```json
[
  {
    "id": 4,
    "name": "ΔΗΜΗΤΡΙΟΣ",
    "surname": "ΑΒΡΑΜΟΠΟΥΛΟΣ",
    "fullName": "Αβραμόπουλος Δημήτριος",
    "party": "Νέα Δημοκρατία",
    "district": "Α' Αθηνών",
    "photo": "/uploads/yyyyyyyyyy.jpg",
    "declarations": [
      2016,
      2017,
      2018,
      2019,
      2020
    ]
  },
  {
    "id": 5,
    "name": "ΕΙΡΗΝΗ-ΕΛΕΝΗ",
    "surname": "ΑΓΑΘΟΠΟΥΛΟΥ",
    "fullName": "Αγαθοπούλου Ειρήνη-Ελένη",
    "party": "Συνασπισμός Ριζοσπαστικής Αριστεράς",
    "district": "Κιλκίς",
    "photo": "/uploads/xxxxxxxxx.jpg",
    "declarations": [
      2016,
      2017,
    ]
  }
]
```

### Request about a specific politician

Users can fetch data about a specific politician based on politician's id like the example `https://api.wealthobserver.gr/politicians/643`. The following example response has data for only one declaration.

```json
{
  "politician": {
    "id": "643",
    "name": "ΑΘΑΝΑΣΙΟΣ",
    "surname": "ΠΑΠΑΔΟΠΟΥΛΟΣ",
    "fullName": "Αθανάσιος (Σάκης) Παπαδόπουλος",
    "party": "Συνασπισμός Ριζοσπαστικής Αριστεράς",
    "partyId": 2,
    "district": "Τρικάλων",
    "photo": "/uploads/2fb1d49f947d4a26a393ed3c0d41e08a.jpg",
    "position": [
      {
        "position": "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΒΟΥΛΕΥΤΗΣ",
        "start_date": "2015-01-25 00:00:00",
        "end_date": ""
      }
    ]
  },
  "peak": {
    "incomes": 155202.93,
    "savings": 103081.47,
    "investments": 423.87,
    "loans": 0,
    "companies": 0
  },
  "declarations": [
    {
      "id": 647,
      "year": 2016,
      "pdf": "http://www.hellenicparliament.gr/userfiles/pothen/xrhsh2015_etos2016/PAPADOPOYLOS_ATHANASIOS_639316_2016.pdf",
      "sum": {
        "savings": 9097.05,
        "incomes": 104936.99,
        "loans": 0,
        "investments": 382.68,
        "companies": 0
      },
      "savings": [
        {
          "amount": 52.78,
          "bank": "EUROBANK"
        },
        {
          "amount": 3566.52,
          "bank": "ΕΘΝΙΚΗ ΤΡΑΠΕΖΑ"
        },
        {
          "amount": 44.24,
          "bank": "ΤΡΑΠΕΖΑ ΘΕΣΣΑΛΙΑΣ"
        },
        {
          "amount": 86.71000000000001,
          "bank": "ALPHA BANK"
        },
        {
          "amount": 445.47999999999996,
          "bank": "ΤΡΑΠΕΖΑ ΠΕΙΡΑΙΩΣ"
        },
        {
          "amount": 4901.320000000001,
          "bank": "ATTICA BANK"
        }
      ],
      "loans": [],
      "investments": [
        {
          "id": 1867,
          "spouse": false,
          "type": "ΑΛΛΗ ΠΕΡΙΠΤΩΣΗ",
          "title": "ΣΥΝΕΤΑΙΡΙΣΤΙΚΗ ΜΕΡΙΔΑ",
          "amount": 1,
          "valuation": 66.09,
          "value": "",
          "declaration": 647,
          "titleoriginal": "ΣΥΝΕΤΑΙΡΙΣΤΙΚΗ ΜΕΡΙΔΑ",
          "created_by": "",
          "updated_by": ""
        },
        {
          "id": 1868,
          "spouse": true,
          "type": "ΜΕΡΙΔΙΑ ΑΜΟΙΒΑΙΩΝ ΚΕΦΑΛΑΙΩΝ",
          "title": "INTERAMERICAN ΔΥΝΑΜΙΚΟ ΜΕΤΟΧΙΚΟ ΕΣΩΤΕΡΙΚΟΥ",
          "amount": 36.74,
          "valuation": 316.59,
          "value": "",
          "declaration": 647,
          "titleoriginal": "INTERAMERICAN ΔΥΝΑΜΙΚΟ ΜΕΤΟΧΙΚΟ ΕΣΩΤΕΡΙΚΟΥ",
          "created_by": "",
          "updated_by": ""
        }
      ],
      "companies": [],
      "vehicles": [
        {
          "id": 1437,
          "type": "ΕΠΙΒΑΤΙΚΟ Ι.Χ.",
          "declaration": 647,
          "power": 1597,
          "created_by": "",
          "updated_by": ""
        },
        {
          "id": 1438,
          "type": "ΕΠΙΒΑΤΙΚΟ Ι.Χ.",
          "declaration": 647,
          "power": 2393,
          "created_by": "",
          "updated_by": ""
        }
      ],
      "incomes": [
        {
          "amount": 54819.490000000005,
          "type": "Συνολικό καθαρό εισόδημα"
        },
        {
          "amount": 30.340000000000003,
          "type": "Μερίσματα, τόκοι, δικαιώματα"
        },
        {
          "amount": 48137.17,
          "type": "Άλλη περίπτωση"
        },
        {
          "amount": 1949.99,
          "type": "Από Ακίνητα"
        }
      ],
      "lands": [
        {
          "id": 9170,
          "spouse": false,
          "country": "ΕΛΛΑΔΑ",
          "municipality": "ΠΙΕΡΙΑΣ",
          "type": "Καλλιέργεια",
          "land_area": 64937,
          "building_area": "",
          "year": 1993,
          "pool": 0,
          "source": "ΑΓΟΡΑ",
          "declaration": 647,
          "floor": "",
          "type_id": "",
          "created_by": "",
          "updated_by": ""
        },
        {
          "id": 9171,
          "spouse": false,
          "country": "ΕΛΛΑΔΑ",
          "municipality": "ΤΡΙΚΑΛΩΝ",
          "type": "Μονοκατοικία",
          "land_area": 0,
          "building_area": 74.61,
          "year": 2012,
          "pool": 0,
          "source": "ΚΛΗΡΟΝΟΜΙΑ",
          "declaration": 647,
          "floor": 0,
          "type_id": "",
          "created_by": "",
          "updated_by": ""
        },
        {
          "id": 9172,
          "spouse": false,
          "country": "ΕΛΛΑΔΑ",
          "municipality": "ΤΡΙΚΑΛΩΝ",
          "type": "Βοσκότοπος",
          "land_area": 6022,
          "building_area": "",
          "year": 2012,
          "pool": 0,
          "source": "ΚΛΗΡΟΝΟΜΙΑ",
          "declaration": 647,
          "floor": "",
          "type_id": "",
          "created_by": "",
          "updated_by": ""
        },
        {
          "id": 9173,
          "spouse": true,
          "country": "ΕΛΛΑΔΑ",
          "municipality": "ΛΑΡΙΣΗΣ",
          "type": "Καλλιέργεια",
          "land_area": 79904,
          "building_area": "",
          "year": 2013,
          "pool": 0,
          "source": "ΚΛΗΡΟΝΟΜΙΑ",
          "declaration": 647,
          "floor": "",
          "type_id": "",
          "created_by": "",
          "updated_by": ""
        },
        {
          "id": 9174,
          "spouse": false,
          "country": "ΕΛΛΑΔΑ",
          "municipality": "ΤΡΙΚΑΛΩΝ",
          "type": "Μονοκατοικία",
          "land_area": 110.78,
          "building_area": 67,
          "year": 1968,
          "pool": 0,
          "source": "ΓΟΝΙΚΗ ΠΑΡΟΧΗ",
          "declaration": 647,
          "floor": 1,
          "type_id": "",
          "created_by": "",
          "updated_by": ""
        },
        {
          "id": 9175,
          "spouse": true,
          "country": "ΕΛΛΑΔΑ",
          "municipality": "ΤΡΙΚΑΛΩΝ",
          "type": "Μονοκατοικία",
          "land_area": 320,
          "building_area": 148,
          "year": 1980,
          "pool": 0,
          "source": "ΑΝΕΓΕΡΣΗ, ΚΛΗΡΟΝΟΜΙΑ",
          "declaration": 647,
          "floor": 1,
          "type_id": "",
          "created_by": "",
          "updated_by": ""
        }
      ]
    }
  ],
  "years": [
    2016
  ]
}
```

### Request about getting the data of specific declaration of a politician

This could happen by providing the year and politician id. e.g `https://api.wealthobserver.gr/declarations?year=2019&politician=132` or `https://api.wealthobserver.gr/politicians/132?year=2019`,

An example response is the following:

```json
{
"id": 2817,
"year": 2019,
"politician": {
  "id": 132,
  "name": "ΕΥΣΤΑΘΙΑ",
  "surname": "ΓΕΩΡΓΟΠΟΥΛΟΥ",
  "position": [
    {
    "position": "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΒΟΥΛΕΥΤΗΣ",
    "start_date": "2012-05-06 00:00:00",
    "end_date": ""
    }
  ],
  "pdf": "http://www.hellenicparliament.gr/userfiles/pothen/xrhsh2015_etos2016/GEORGOPOYLOY_EYSTATHIA_1202188_2016.pdf",
  "fathersname": "ΕΥΣΤΑΘ",
  "spouse_name": "ΒΑΣΙΛ",
  "spouse_surname": "ΣΑΛΤΑΡΗΣ",
  "spouse_fathersname": "ΓΕΩΡΓΙΟΣ",
  "district": 33,
  "party": 2,
  "full_name": "Γεωργοπούλου-Σαλτάρη Ευσταθία (Έφη)",
  "photo": "/uploads/xxxxxxxxx.jpg"
},
"loans": [ ],
"savings": [
  {
    "id": 36555,
    "spouse": false,
    "bank": "ΕΘΝΙΚΗ ΤΡΑΠΕΖΑ",
    "country": "ΕΛΛΑΔΑ",
    "currency": "ΕΥΡΩ",
    "amount": 32393.48,
    "declaration": 2817
  }
],
"incomes": [],
"companies": [],
"lockers": [],
"vehicles": [],
"lands": [],
```

### Request about politicians' income

An example request url is the following, users can change the year about the year that they prefer.
e.g. `https://api.wealthobserver.gr/declarations/graph?year=2018&type=incomes&_limit=-1`

The example response below has only one politician inside the items array.

```json
{
  "items": [
    {
      "id": 1,
      "name": "Κωνσταντίνα",
      "surname": "Κούνεβα",
      "fullName": "Κωσταντίνα Κούνεβα",
      "party": 2,
      "photo": "",
      "position": "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΕΥΡΩΒΟΥΛΕΥΤΗΣ",
      "extra": {
        "Μερίσματα, τόκοι, δικαιώματα": {
          "total": 25.42,
          "spouse": 0,
          "main": 25.42
        },
        "Άλλη περίπτωση": {
          "total": 102492.12,
          "spouse": 0,
          "main": 102492.12
        },
        "Συνολικό καθαρό εισόδημα": {
          "total": 3404.14,
          "spouse": 0,
          "main": 3404.14
        },
        "Αλλοδαπής προέλευσης": {
          "total": 1447.62,
          "spouse": 0,
          "main": 1447.62
        },
        "sum": {
          "total": 107369.3,
          "spouse": 0,
          "main": 107369.3
        }
      },
      "incomes": {
        "total": 107369.3,
        "spouse": 0,
        "main": 107369.3
      }
    },
  ],
  "filters": [
    "ΜΕΡΙΣΜΑΤΑ, ΤΟΚΟΙ, ΔΙΚΑΙΩΜΑΤΑ",
    "ΑΛΛΗ ΠΕΡΙΠΤΩΣΗ",
    "ΣΥΝΟΛΙΚΟ ΚΑΘΑΡΟ ΕΙΣΟΔΗΜΑ ΑΠΟ ΜΙΣΘΩΤΕΣ ΥΠΗΡΕΣΙΕΣ, ΕΠΙΔΟΜΑΤΑ,ΠΡΟΣΘΕΤΕΣ ΑΜΟΙΒΕΣ Κ.Λ.Π.(ΦΟΡΟΛΟΓΟΥΜΕΝΑ, ΦΟΡΟΛΟΓΟΥΜΕΝΑ ΜΕ ΕΙΔΙΚΟ ΤΡΟΠΟ, ΦΟΡΟΛΟΓ. ΑΥΤΟΤΕΛΩΣ, ΑΦΟΡΟΛΟΓΗΤΑ)",
    "ΑΛΛΟΔΑΠΗΣ ΠΡΟΕΛΕΥΣΗΣ",
    "ΕΙΣΟΔΗΜΑ ΑΠΟ ΕΠΙΧΕΙΡΗΜΑΤΙΚΗ ΔΡΑΣΤΗΡΙΟΤΗΤΑ",
    "ΑΝΑΔΡΟΜΙΚΑ ΠΡΟΗΓΟΥΜΕΝΩΝ ΕΤΩΝ",
    "ΑΠΟ ΑΚΙΝΗΤΑ",
    "ΔΩΡΕΕΣ",
    "ΕΙΣΟΔΗΜΑ ΑΠΟ ΑΓΡΟΤΙΚΗ ΕΠΙΧΕΙΡΗΜΑΤΙΚΗ ΔΡΑΣΤΗΡΙΤΟΤΗΤΑ",
    "ΤΟΚΟΙ ΚΑΤΑΘΕΣΕΩΝ ΤΡΑΠΕΖΩΝ ΗΜΕΔΑΠΗΣ ΠΡΟΕΛΕΥΣΗΣ",
    "ΔΙΑΘΕΣΗ ΠΕΡΙΟΥΣΙΑΚΩΝ ΣΤΟΙΧΕΙΩΝ",
    "ΕΙΣΟΔΗΜΑ ΑΠΟ ΥΠΕΡΑΞΙΑ ΜΕΤΑΒΙΒΑΣΗΣ ΚΕΦΑΛΑΙΟΥ",
    "ΟΙΚΟΝΟΜΙΚΕΣ ΕΝΙΣΧΥΣΕΙΣ",
    "ΔΑΝΕΙΑ",
    "ΕΠΑΝΑΠΑΤΡΙΖΟΜΕΝΑ ΚΕΦΑΛΑΙΑ"
  ],
  "parties": [
    {
      "id": 7,
      "name": "Ελληνική Λύση"
    },
    {
      "id": 2,
      "name": "Συνασπισμός Ριζοσπαστικής Αριστεράς"
    },
    {
      "id": 1,
      "name": "Νέα Δημοκρατία"
    },
    {
      "id": 10,
      "name": "ΜέΡΑ25"
    },
  ],
  "positions": [
    "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΕΥΡΩΒΟΥΛΕΥΤΗΣ",
    "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΒΟΥΛΕΥΤΗΣ",
    "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΥΦΥΠΟΥΡΓΟΣ",
    "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΑΝΑΠΛΗΡΩΤΗΣ ΥΠΟΥΡΓΟΣ",
    "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΥΠΟΥΡΓΟΣ",
    "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΔΙΑΧΕΙΡΙΣΤΗΣ ΟΙΚΟΝΟΜΙΚΩΝ ΚΟΜΜΑΤΟΣ ΠΟΥ ΕΚΠΡΟΣΩΠΕΙΤΑΙ ΣΤΟ ΕΘΝΙΚΟ Η ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ Η ΛΑΜΒΑΝΕΙ ΚΡΑΤΙΚΗ ΧΡΗΜΑΤΟΔΟΤΗΣΗ",
    "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΑΡΧΗΓΟΣ ΠΟΛΙΤΙΚΟΥ ΚΟΜΜΑΤΟΣ ΠΟΥ ΕΚΠΡΟΣΩΠΕΙΤΑΙ ΣΤΟ ΕΘΝΙΚΟ Η ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ Η ΛΑΜΒΑΝΕΙ ΚΡΑΤΙΚΗ ΧΡΗΜΑΤΟΔΟΤΗΣΗ",
    "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΓΕΝΙΚΟΣ ΓΡΑΜΜΑΤΕΑΣ ΒΟΥΛΗΣ Η ΓΕΝΙΚΗΣ ΚΥΒΕΡΝΗΣΗΣ",
    "ΕΘΝΙΚΟ, ΕΥΡΩΠΑΙΚΟ ΚΟΙΝΟΒΟΥΛΙΟ, ΚΥΒΕΡΝΗΣΗ ΠΡΩΘΥΠΟΥΡΓΟΣ"
  ]
},
```

The parties array on response have the id of the available parties, also every item have the id of the party that the politician belongs.

### Request about politicians' savings

An example request url is the following, users can change the year about the year that they prefer.
e.g. `https://api.wealthobserver.gr/declarations/graph?year=2019&type=savings&_limit=-1`

The response of type savings is almost the same as above. The only difference is that the filters have the available banks in all declarations of the current year. An example is the following:

```json
{
  "filters": [
    "KBC BRUSSELS",
    "ΤΡΑΠΕΖΑ ΠΕΙΡΑΙΩΣ ΒΟΥΛΓΑΡΙΑΣ",
    "LCL",
    "ΤΡΑΠΕΖΑ ΠΕΙΡΑΙΩΣ",
    "ΤΡΑΠΕΖΑ EUROBANK",
    "EUROBANK",
    "Ε.Τ.Ε",
    "ETE",
    "ΕΘΝΙΚΗ ΤΡΑΠΕΖΑ",
    "ΠΕΙΡΑΙΩΣ",
    "ALPHA",
    "ΕΘΝΙΚΗ"
  ]
}
```

### Request about politicians' investments, lands, loans, companies,

These requests and their responses are almost the same as above. Users could change the type and the year. For example:

`https://api.wealthobserver.gr/declarations/graph?year=2019&type=investments&_limit=-1`
`https://api.wealthobserver.gr/declarations/graph?year=2019&type=lands&_limit=-1`
`https://api.wealthobserver.gr/declarations/graph?year=2019&type=loans&_limit=-1`
`https://api.wealthobserver.gr/declarations/graph?year=2019&type=companies&_limit=-1`


### Notifications request

As the users are selecting politicians, they can have notifications if these politicians have the top values in their declarations
for the selected year. The endpoint that checks for notifications for a politician for a specific year

`https://api.wealthobserver.gr/politicians/:politicianId/select/:year`

The response is the following

if year is not supported

```json
"success": false
```

if request was successful but not any notification have found

```json
"success": true
```

if request was successful and some notifications have found. The reasons array have the values that have been checked for the current politicians.
In investments, lands & companies in reasons array maybe have one or two values. For example a politicians belongs to the top 30 politicians with the more building area but not with landArea like politician with id `69`. On incomes, savings and loans the reasons have only the value "amount"

```json
"success": true,
"notifications": {
  "incomes":{
    "reasons":["amount"]
  },
  "savings":{
    "reasons":["amount"]
  },
  "loans":{
    "reasons":["amount"]
  },
  "investments":{
    "reasons":["valuation","value"]
  },
  "lands":{
    "reasons":["buildingArea", "landArea"]
  },
  "companies":{
    "reasons":["startingFund","fundNow"]
  }
}
```

### Example of other requests
 - `https://api.wealthobserver.gr/politicians?name_contains=ΜΙΧΑΗΛ`
 - `https://api.wealthobserver.gr/politicians?name_contains=ΜΙΧΑΗΛ&surname_contains=ΠΑΠΑΔΟΠΟΥΛΟΣ`
 - `https://api.wealthobserver.gr/declarations?year=2018&_limit=2&politician.party=1`
