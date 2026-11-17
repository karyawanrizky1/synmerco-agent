# Branch location data check — Burke & Herbert Bank & Trust Company

Bank: Burke & Herbert Bank & Trust Company, FDIC CERT 11578, Virginia. Job job_2d7a231154ca4170. Escrow esc_21e100923e3747a895409c15 (FUNDED, net $4.75). Seller: Karyawanrizky1 (did:pkh:eip155:8453:0xa12Ed7470708Fc1fb153B19D3dB9e313E36F1ba6).

Task: every Virginia branch of this bank from FDIC BankFind, geocoded with the US Census Geocoder, checked for county agreement (GEOID = STCNTY) and distance (haversine, Earth radius 6,371 km). Flags: no match; county differs; over 1 km apart. Three timed pulls, 24 hours apart, each with its own CSV data file attached under Rule 25.

## Sources and method

- FDIC BankFind, `api.fdic.gov/banks/locations`, filters `CERT:11578 AND STALP:VA`, fields NAME, OFFNAME, UNINUM, ADDRESS, CITY, STALP, ZIP, COUNTY, STCNTY, LATITUDE, LONGITUDE, limit 100, format json. No key.
- US Census Geocoder, `geocoding.geo.census.gov/geocoder/geographies/onelineaddress`, one line ADDRESS, CITY, STALP ZIP; benchmark Public_AR_Current, vintage Current_Current, layers Counties, format json; one request per second. No key.
- Match: yes when the geocoder returns at least one address match; the first match is used. Distance: haversine between the FDIC point and the geocoder point. Figures: 2 decimals, half away from zero, from unrounded values.
- Only the sources listed here were used. No login-only or paid source. No advice, opinions or forecasts beyond what the sources state.

## Counts

| Pull | Branches | Match yes | Match no | Match rate | No match | County differs | Over 1 km |
|---|---|---|---|---|---|---|---|
| PULL 1 | 40 | 37 | 3 | 92.50% | 3 | 0 | 1 |
| PULL 2 | 40 | 36 | 4 | 90.00% | 4 | 0 | 1 |
| PULL 3 | 40 | 37 | 3 | 92.50% | 3 | 0 | 1 |

PULL 1 note: 2026-11-15 05:15:50 UTC. PULL 2 note: 2026-11-16 05:24:28 UTC (24h 08m 38s after PULL 1). PULL 3 note: 2026-11-17 05:35:09 UTC (24h 10m 41s after PULL 2). Earliest submit 2026-11-17 03:42:46 UTC; deliver by 2026-11-19 11:42:46 UTC.

## Flagged branches

Every branch with a flag in any pull, with both addresses and the distance. No branch ever had a county-differ flag: for every matched branch in every pull, GEOID equals STCNTY.

### PULL 1 — 4 flagged of 40 branches

- uninum 508194, CENTREVILLE BRANCH, FDIC: 14122 Lee Highway, Fairfax, 22031, STCNTY 51059, FDIC (38.860077, -77.259257); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 518473, SPOTSYLVANIA COURTHOUSE BRANCH, FDIC: 7415 Laughlin Blvd, Spotsylvania Courthouse, 22553, STCNTY 51177, FDIC (38.205925000000036, -77.57299499999993); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 663907, MANASSAS BRANCH, FDIC: 9757 Phair Way, Manassas, 20110, STCNTY 51683, FDIC (38.7515731, -77.478839); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 8219, MONTEREY BRANCH, FDIC: 195  West Main Strret, Monterey, 24465, STCNTY 51091, FDIC (38.416626, -79.559836); match yes; matched: 195 W MAIN ST, MONTEREY, VA, 24465; geocoder (38.413067628384, -79.582632843174), GEOID 51091; 2.03 km apart; flags: over 1 km apart.

### PULL 2 — 5 flagged of 40 branches

- uninum 225047, COOPER ROAD BRANCH, FDIC: 8736 Cooper Rd, Alexandria, 22309, STCNTY 51059, FDIC (38.71964620832338, -77.12453736789736); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 508194, CENTREVILLE BRANCH, FDIC: 14122 Lee Highway, Fairfax, 22031, STCNTY 51059, FDIC (38.860077, -77.259257); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 518473, SPOTSYLVANIA COURTHOUSE BRANCH, FDIC: 7415 Laughlin Blvd, Spotsylvania Courthouse, 22553, STCNTY 51177, FDIC (38.205925000000036, -77.57299499999993); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 663907, MANASSAS BRANCH, FDIC: 9757 Phair Way, Manassas, 20110, STCNTY 51683, FDIC (38.7515731, -77.478839); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 8219, MONTEREY BRANCH, FDIC: 195  West Main Strret, Monterey, 24465, STCNTY 51091, FDIC (38.416626, -79.559836); match yes; matched: 195 W MAIN ST, MONTEREY, VA, 24465; geocoder (38.413067628384, -79.582632843174), GEOID 51091; 2.03 km apart; flags: over 1 km apart.

### PULL 3 — 4 flagged of 40 branches

- uninum 508194, CENTREVILLE BRANCH, FDIC: 14122 Lee Highway, Fairfax, 22031, STCNTY 51059, FDIC (38.860077, -77.259257); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 518473, SPOTSYLVANIA COURTHOUSE BRANCH, FDIC: 7415 Laughlin Blvd, Spotsylvania Courthouse, 22553, STCNTY 51177, FDIC (38.205925000000036, -77.57299499999993); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 663907, MANASSAS BRANCH, FDIC: 9757 Phair Way, Manassas, 20110, STCNTY 51683, FDIC (38.7515731, -77.478839); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 8219, MONTEREY BRANCH, FDIC: 195  West Main Strret, Monterey, 24465, STCNTY 51091, FDIC (38.416626, -79.559836); match yes; matched: 195 W MAIN ST, MONTEREY, VA, 24465; geocoder (38.413067628384, -79.582632843174), GEOID 51091; 2.03 km apart; flags: over 1 km apart.

## Changes

### PULL 2 vs PULL 1

New: 0 (none). Gone: 0 (none). Changed: 1 branch(es). Row counts: 40 = 40 + 0 - 0.

- uninum 225047:
  - match: yes -> no
  - matched address: 8736 COOPER RD, ALEXANDRIA, VA, 22309 -> (empty)
  - geo lat: 38.719591743654 -> (empty)
  - geo lon: -77.124146538216 -> (empty)
  - geoid: 51059 -> (empty)
  - km apart: 0.03 -> (empty)
  - flags: (empty) -> no match

### PULL 3 vs PULL 2

New: 0 (none). Gone: 0 (none). Changed: 1 branch(es). Row counts: 40 = 40 + 0 - 0.

- uninum 225047:
  - match: no -> yes
  - matched address: (empty) -> 8736 COOPER RD, ALEXANDRIA, VA, 22309
  - geo lat: (empty) -> 38.719591743654
  - geo lon: (empty) -> -77.124146538216
  - geoid: (empty) -> 51059
  - km apart: (empty) -> 0.03
  - flags: no match -> (empty)

## PROOF

Every request below is listed with its UTC time (the HTTP Date response header). FDIC first-request HTTP Date per pull: PULL 1 Sun, 15 Nov 2026 04:43:33 GMT; PULL 2 Mon, 16 Nov 2026 05:21:11 GMT; PULL 3 Tue, 17 Nov 2026 05:31:34 GMT. Each pull's first-request HTTP Date is later than the previous pull's.

### PULL 1 requests

- FDIC: https://api.fdic.gov/banks/locations?filters=CERT%3A11578%20AND%20STALP%3AVA&fields=NAME,OFFNAME,UNINUM,ADDRESS,CITY,STALP,ZIP,COUNTY,STCNTY,LATITUDE,LONGITUDE&limit=100&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:33 GMT
- PULL 1 | uninum 212907 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=148+Ivanhoe+Rd%2C+Max+Meadows%2C+VA+24360&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:33 GMT
- PULL 1 | uninum 225042 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=306+E+Monroe+Ave%2C+Alexandria%2C+VA+22301&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:35 GMT
- PULL 1 | uninum 225043 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1775+Jamieson+Ave%2C+Alexandria%2C+VA+22314&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:37 GMT
- PULL 1 | uninum 225044 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=5731+Telegraph+Rd%2C+Alexandria%2C+VA+22303&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:39 GMT
- PULL 1 | uninum 225047 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=8736+Cooper+Rd%2C+Alexandria%2C+VA+22309&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:41 GMT
- PULL 1 | uninum 225048 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=5705+Seminary+Rd%2C+Falls+Church%2C+VA+22041&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:42 GMT
- PULL 1 | uninum 225049 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=2604+Sherwood+Hall+Ln%2C+Alexandria%2C+VA+22306&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:44 GMT
- PULL 1 | uninum 225051 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1705+Fern+St%2C+Alexandria%2C+VA+22302&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:46 GMT
- PULL 1 | uninum 225052 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=225+W+Broad+St%2C+Falls+Church%2C+VA+22046&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:48 GMT
- PULL 1 | uninum 263661 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=108+Spruce+St%2C+Bluefield%2C+VA+24605&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:50 GMT
- PULL 1 | uninum 358770 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=6200+Backlick+Rd%2C+Springfield%2C+VA+22150&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:52 GMT
- PULL 1 | uninum 360368 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=6210+Inter+Parcel+Rd%2C+Alexandria%2C+VA+22315&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:53 GMT
- PULL 1 | uninum 363744 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=204+Catoctin+Cir+Se%2C+Leesburg%2C+VA+20175&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:55 GMT
- PULL 1 | uninum 419173 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1925+Stone+Spring+Rd%2C+Rockingham%2C+VA+22801&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:57 GMT
- PULL 1 | uninum 429547 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9406+Sam+Snead+Hwy%2C+Hot+Springs%2C+VA+24445&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:59 GMT
- PULL 1 | uninum 432308 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=14008+Smoketown+Rd%2C+Woodbridge%2C+VA+22192&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:01 GMT
- PULL 1 | uninum 442397 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=224+S+Main+St%2C+Harrisonburg%2C+VA+22801&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:02 GMT
- PULL 1 | uninum 445564 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=251+W+Lee+Hwy%2C+Warrenton%2C+VA+20186&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:04 GMT
- PULL 1 | uninum 466498 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=4235+Annandale+Rd%2C+Annandale%2C+VA+22003&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:06 GMT
- PULL 1 | uninum 469496 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=410+William+St%2C+Fredericksburg%2C+VA+22401&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:08 GMT
- PULL 1 | uninum 47074 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=200+Peppers+Ferry+Rd%2C+Wytheville%2C+VA+24382&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:10 GMT
- PULL 1 | uninum 481684 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9103+Centreville+Rd%2C+Manassas%2C+VA+20110&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:12 GMT
- PULL 1 | uninum 488794 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=332+Maple+Ave+E%2C+Vienna%2C+VA+22180&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:14 GMT
- PULL 1 | uninum 497232 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9516+Old+Keene+Mill+Rd%2C+Burke%2C+VA+22015&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:16 GMT
- PULL 1 | uninum 497950 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=23+Scenic+Hwy%2C+Churchville%2C+VA+24421&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:17 GMT
- PULL 1 | uninum 508194 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=14122+Lee+Highway%2C+Fairfax%2C+VA+22031&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:19 GMT
- PULL 1 | uninum 517570 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=3030+Clarendon+Blvd%2C+Arlington%2C+VA+22201&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:21 GMT
- PULL 1 | uninum 517927 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=6705+Whittier+Ave%2C+Mclean%2C+VA+22101&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:23 GMT
- PULL 1 | uninum 518473 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=7415+Laughlin+Blvd%2C+Spotsylvania+Courthouse%2C+VA+22553&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:25 GMT
- PULL 1 | uninum 528023 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=4605+Daisy+Reid+Ave%2C+Woodbridge%2C+VA+22192&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:27 GMT
- PULL 1 | uninum 589858 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=4210+Plank+Rd%2C+Fredericksburg%2C+VA+22407&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:29 GMT
- PULL 1 | uninum 625459 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=100+Akers+Farm+Rd%2C+Christiansburg%2C+VA+24073&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:31 GMT
- PULL 1 | uninum 626395 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=12030+Sunrise+Valley+Dr%2C+Reston%2C+VA+20191&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:33 GMT
- PULL 1 | uninum 637091 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=2521+Cowan+Blvd%2C+Fredericksburg%2C+VA+22401&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:35 GMT
- PULL 1 | uninum 638450 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1821+Michael+Faraday+Dr%2C+Reston%2C+VA+20190&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:37 GMT
- PULL 1 | uninum 661496 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=2065+Huguenot+Road%2C+North+Chesterfield%2C+VA+23235&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:39 GMT
- PULL 1 | uninum 663907 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9757+Phair+Way%2C+Manassas%2C+VA+20110&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:41 GMT
- PULL 1 | uninum 7397 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=100+S+Fairfax+St%2C+Alexandria%2C+VA+22314&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:43 GMT
- PULL 1 | uninum 74896 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=100+W+Jubal+Early+Dr%2C+Winchester%2C+VA+22601&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:45 GMT
- PULL 1 | uninum 8219 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=195++West+Main+Strret%2C+Monterey%2C+VA+24465&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:47 GMT

### PULL 1 flagged-branch excerpts (FDIC record + geocoder first match, as returned)

- PULL 1 | uninum 508194 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "508194", "OFFNAME": "CENTREVILLE BRANCH", "ADDRESS": "14122 Lee Highway", "CITY": "Fairfax", "STALP": "VA", "ZIP": "22031", "STCNTY": "51059", "LATITUDE": "38.860077", "LONGITUDE": "-77.259257"}
```
- PULL 1 | uninum 508194 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"14122 Lee Highway, Fairfax, VA 22031"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 1 | uninum 518473 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "518473", "OFFNAME": "SPOTSYLVANIA COURTHOUSE BRANCH", "ADDRESS": "7415 Laughlin Blvd", "CITY": "Spotsylvania Courthouse", "STALP": "VA", "ZIP": "22553", "STCNTY": "51177", "LATITUDE": "38.205925000000036", "LONGITUDE": "-77.57299499999993"}
```
- PULL 1 | uninum 518473 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"7415 Laughlin Blvd, Spotsylvania Courthouse, VA 22553"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 1 | uninum 663907 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "663907", "OFFNAME": "MANASSAS BRANCH", "ADDRESS": "9757 Phair Way", "CITY": "Manassas", "STALP": "VA", "ZIP": "20110", "STCNTY": "51683", "LATITUDE": "38.7515731", "LONGITUDE": "-77.478839"}
```
- PULL 1 | uninum 663907 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"9757 Phair Way, Manassas, VA 20110"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 1 | uninum 8219 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "8219", "OFFNAME": "MONTEREY BRANCH", "ADDRESS": "195  West Main Strret", "CITY": "Monterey", "STALP": "VA", "ZIP": "24465", "STCNTY": "51091", "LATITUDE": "38.416626", "LONGITUDE": "-79.559836"}
```
- PULL 1 | uninum 8219 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"195  West Main Strret, Monterey, VA 24465"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[{"tigerLine":{"side":"L","tigerLineId":"172822818"},"geographies":{"Counties":[{"GEOID":"51091","CENTLAT":"+38.3622579","AREAWATER":1791756,"STATE":"51","BASENAME":"Highland","OID":"27590765115510","LSADC":"06","FUNCSTAT":"A","INTPTLAT":"+38.3662431","NAME":"Highland County","OBJECTID":1446,"CENTLON":"-079.5685507","COUNTYCC":"H1","COUNTYNS":"01673774","AREALAND":1075266882,"INTPTLON":"-079.5644718","MTFCC":"G4020","COUNTY":"091"}]},"coordinates":{"x":-79.582632843174,"y":38.413067628384},"addressComponents":{"zip":"24465","streetName":"MAIN","preType":"","city":"MONTEREY","preDirection":"W","suffixDirection":"","fromAddress":"195","state":"VA","suffixType":"ST","toAddress":"299","suffixQualifier":"","preQualifier":""},"matchedAddress":"195 W MAIN ST, MONTEREY, VA, 24465"}]}}
```

### PULL 2 requests

- FDIC: https://api.fdic.gov/banks/locations?filters=CERT%3A11578%20AND%20STALP%3AVA&fields=NAME,OFFNAME,UNINUM,ADDRESS,CITY,STALP,ZIP,COUNTY,STCNTY,LATITUDE,LONGITUDE&limit=100&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:11 GMT
- PULL 2 | uninum 212907 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=148+Ivanhoe+Rd%2C+Max+Meadows%2C+VA+24360&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:12 GMT
- PULL 2 | uninum 225042 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=306+E+Monroe+Ave%2C+Alexandria%2C+VA+22301&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:14 GMT
- PULL 2 | uninum 225043 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1775+Jamieson+Ave%2C+Alexandria%2C+VA+22314&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:16 GMT
- PULL 2 | uninum 225044 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=5731+Telegraph+Rd%2C+Alexandria%2C+VA+22303&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:23 GMT
- PULL 2 | uninum 225047 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=8736+Cooper+Rd%2C+Alexandria%2C+VA+22309&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status: request failed (HTTP Error 502: ) — no response, no HTTP Date recorded
- PULL 2 | uninum 225048 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=5705+Seminary+Rd%2C+Falls+Church%2C+VA+22041&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:46 GMT
- PULL 2 | uninum 225049 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=2604+Sherwood+Hall+Ln%2C+Alexandria%2C+VA+22306&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:48 GMT
- PULL 2 | uninum 225051 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1705+Fern+St%2C+Alexandria%2C+VA+22302&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:50 GMT
- PULL 2 | uninum 225052 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=225+W+Broad+St%2C+Falls+Church%2C+VA+22046&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:51 GMT
- PULL 2 | uninum 263661 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=108+Spruce+St%2C+Bluefield%2C+VA+24605&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:53 GMT
- PULL 2 | uninum 358770 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=6200+Backlick+Rd%2C+Springfield%2C+VA+22150&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:02 GMT
- PULL 2 | uninum 360368 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=6210+Inter+Parcel+Rd%2C+Alexandria%2C+VA+22315&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:04 GMT
- PULL 2 | uninum 363744 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=204+Catoctin+Cir+Se%2C+Leesburg%2C+VA+20175&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:05 GMT
- PULL 2 | uninum 419173 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1925+Stone+Spring+Rd%2C+Rockingham%2C+VA+22801&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:13 GMT
- PULL 2 | uninum 429547 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9406+Sam+Snead+Hwy%2C+Hot+Springs%2C+VA+24445&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:15 GMT
- PULL 2 | uninum 432308 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=14008+Smoketown+Rd%2C+Woodbridge%2C+VA+22192&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:17 GMT
- PULL 2 | uninum 442397 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=224+S+Main+St%2C+Harrisonburg%2C+VA+22801&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:18 GMT
- PULL 2 | uninum 445564 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=251+W+Lee+Hwy%2C+Warrenton%2C+VA+20186&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:20 GMT
- PULL 2 | uninum 466498 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=4235+Annandale+Rd%2C+Annandale%2C+VA+22003&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:22 GMT
- PULL 2 | uninum 469496 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=410+William+St%2C+Fredericksburg%2C+VA+22401&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:23 GMT
- PULL 2 | uninum 47074 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=200+Peppers+Ferry+Rd%2C+Wytheville%2C+VA+24382&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:25 GMT
- PULL 2 | uninum 481684 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9103+Centreville+Rd%2C+Manassas%2C+VA+20110&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:26 GMT
- PULL 2 | uninum 488794 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=332+Maple+Ave+E%2C+Vienna%2C+VA+22180&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:28 GMT
- PULL 2 | uninum 497232 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9516+Old+Keene+Mill+Rd%2C+Burke%2C+VA+22015&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:30 GMT
- PULL 2 | uninum 497950 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=23+Scenic+Hwy%2C+Churchville%2C+VA+24421&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:31 GMT
- PULL 2 | uninum 508194 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=14122+Lee+Highway%2C+Fairfax%2C+VA+22031&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:34 GMT
- PULL 2 | uninum 517570 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=3030+Clarendon+Blvd%2C+Arlington%2C+VA+22201&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:36 GMT
- PULL 2 | uninum 517927 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=6705+Whittier+Ave%2C+Mclean%2C+VA+22101&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:38 GMT
- PULL 2 | uninum 518473 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=7415+Laughlin+Blvd%2C+Spotsylvania+Courthouse%2C+VA+22553&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:39 GMT
- PULL 2 | uninum 528023 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=4605+Daisy+Reid+Ave%2C+Woodbridge%2C+VA+22192&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:41 GMT
- PULL 2 | uninum 589858 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=4210+Plank+Rd%2C+Fredericksburg%2C+VA+22407&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:42 GMT
- PULL 2 | uninum 625459 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=100+Akers+Farm+Rd%2C+Christiansburg%2C+VA+24073&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:44 GMT
- PULL 2 | uninum 626395 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=12030+Sunrise+Valley+Dr%2C+Reston%2C+VA+20191&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:46 GMT
- PULL 2 | uninum 637091 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=2521+Cowan+Blvd%2C+Fredericksburg%2C+VA+22401&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:47 GMT
- PULL 2 | uninum 638450 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1821+Michael+Faraday+Dr%2C+Reston%2C+VA+20190&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:49 GMT
- PULL 2 | uninum 661496 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=2065+Huguenot+Road%2C+North+Chesterfield%2C+VA+23235&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:50 GMT
- PULL 2 | uninum 663907 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9757+Phair+Way%2C+Manassas%2C+VA+20110&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:52 GMT
- PULL 2 | uninum 7397 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=100+S+Fairfax+St%2C+Alexandria%2C+VA+22314&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:54 GMT
- PULL 2 | uninum 74896 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=100+W+Jubal+Early+Dr%2C+Winchester%2C+VA+22601&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:55 GMT
- PULL 2 | uninum 8219 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=195++West+Main+Strret%2C+Monterey%2C+VA+24465&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:57 GMT

### PULL 2 flagged-branch excerpts (FDIC record + geocoder first match, as returned)

- PULL 2 | uninum 225047 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "225047", "OFFNAME": "COOPER ROAD BRANCH", "ADDRESS": "8736 Cooper Rd", "CITY": "Alexandria", "STALP": "VA", "ZIP": "22309", "STCNTY": "51059", "LATITUDE": "38.71964620832338", "LONGITUDE": "-77.12453736789736"}
```
- PULL 2 | uninum 225047 | Geocoder first match (excerpt, as returned):
```
HTTP Error 502: 
```
- Note PULL 2 uninum 225047: the geocoder request failed with HTTP 502, so no match list was returned and the CSV records match no / flags no match. PULL 1 and PULL 3 both matched this branch (0.03 km apart, GEOID 51059), so the change is a transient source error, not a branch change. Per the TASK, each pull is judged by its own excerpts.
- PULL 2 | uninum 508194 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "508194", "OFFNAME": "CENTREVILLE BRANCH", "ADDRESS": "14122 Lee Highway", "CITY": "Fairfax", "STALP": "VA", "ZIP": "22031", "STCNTY": "51059", "LATITUDE": "38.860077", "LONGITUDE": "-77.259257"}
```
- PULL 2 | uninum 508194 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"14122 Lee Highway, Fairfax, VA 22031"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 2 | uninum 518473 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "518473", "OFFNAME": "SPOTSYLVANIA COURTHOUSE BRANCH", "ADDRESS": "7415 Laughlin Blvd", "CITY": "Spotsylvania Courthouse", "STALP": "VA", "ZIP": "22553", "STCNTY": "51177", "LATITUDE": "38.205925000000036", "LONGITUDE": "-77.57299499999993"}
```
- PULL 2 | uninum 518473 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"7415 Laughlin Blvd, Spotsylvania Courthouse, VA 22553"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 2 | uninum 663907 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "663907", "OFFNAME": "MANASSAS BRANCH", "ADDRESS": "9757 Phair Way", "CITY": "Manassas", "STALP": "VA", "ZIP": "20110", "STCNTY": "51683", "LATITUDE": "38.7515731", "LONGITUDE": "-77.478839"}
```
- PULL 2 | uninum 663907 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"9757 Phair Way, Manassas, VA 20110"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 2 | uninum 8219 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "8219", "OFFNAME": "MONTEREY BRANCH", "ADDRESS": "195  West Main Strret", "CITY": "Monterey", "STALP": "VA", "ZIP": "24465", "STCNTY": "51091", "LATITUDE": "38.416626", "LONGITUDE": "-79.559836"}
```
- PULL 2 | uninum 8219 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"195  West Main Strret, Monterey, VA 24465"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[{"tigerLine":{"side":"L","tigerLineId":"172822818"},"geographies":{"Counties":[{"GEOID":"51091","CENTLAT":"+38.3622579","AREAWATER":1791756,"STATE":"51","BASENAME":"Highland","OID":"27590765115510","LSADC":"06","FUNCSTAT":"A","INTPTLAT":"+38.3662431","NAME":"Highland County","OBJECTID":1446,"CENTLON":"-079.5685507","COUNTYCC":"H1","COUNTYNS":"01673774","AREALAND":1075266882,"INTPTLON":"-079.5644718","MTFCC":"G4020","COUNTY":"091"}]},"coordinates":{"x":-79.582632843174,"y":38.413067628384},"addressComponents":{"zip":"24465","streetName":"MAIN","preType":"","city":"MONTEREY","preDirection":"W","suffixDirection":"","fromAddress":"195","state":"VA","suffixType":"ST","toAddress":"299","suffixQualifier":"","preQualifier":""},"matchedAddress":"195 W MAIN ST, MONTEREY, VA, 24465"}]}}
```

### PULL 3 requests

- FDIC: https://api.fdic.gov/banks/locations?filters=CERT%3A11578%20AND%20STALP%3AVA&fields=NAME,OFFNAME,UNINUM,ADDRESS,CITY,STALP,ZIP,COUNTY,STCNTY,LATITUDE,LONGITUDE&limit=100&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:34 GMT
- PULL 3 | uninum 212907 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=148+Ivanhoe+Rd%2C+Max+Meadows%2C+VA+24360&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:35 GMT
- PULL 3 | uninum 225042 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=306+E+Monroe+Ave%2C+Alexandria%2C+VA+22301&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:37 GMT
- PULL 3 | uninum 225043 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1775+Jamieson+Ave%2C+Alexandria%2C+VA+22314&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:39 GMT
- PULL 3 | uninum 225044 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=5731+Telegraph+Rd%2C+Alexandria%2C+VA+22303&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:40 GMT
- PULL 3 | uninum 225047 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=8736+Cooper+Rd%2C+Alexandria%2C+VA+22309&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:42 GMT
- PULL 3 | uninum 225048 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=5705+Seminary+Rd%2C+Falls+Church%2C+VA+22041&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:43 GMT
- PULL 3 | uninum 225049 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=2604+Sherwood+Hall+Ln%2C+Alexandria%2C+VA+22306&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:45 GMT
- PULL 3 | uninum 225051 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1705+Fern+St%2C+Alexandria%2C+VA+22302&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:46 GMT
- PULL 3 | uninum 225052 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=225+W+Broad+St%2C+Falls+Church%2C+VA+22046&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:49 GMT
- PULL 3 | uninum 263661 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=108+Spruce+St%2C+Bluefield%2C+VA+24605&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:50 GMT
- PULL 3 | uninum 358770 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=6200+Backlick+Rd%2C+Springfield%2C+VA+22150&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:52 GMT
- PULL 3 | uninum 360368 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=6210+Inter+Parcel+Rd%2C+Alexandria%2C+VA+22315&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:53 GMT
- PULL 3 | uninum 363744 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=204+Catoctin+Cir+Se%2C+Leesburg%2C+VA+20175&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:55 GMT
- PULL 3 | uninum 419173 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1925+Stone+Spring+Rd%2C+Rockingham%2C+VA+22801&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:57 GMT
- PULL 3 | uninum 429547 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9406+Sam+Snead+Hwy%2C+Hot+Springs%2C+VA+24445&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:58 GMT
- PULL 3 | uninum 432308 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=14008+Smoketown+Rd%2C+Woodbridge%2C+VA+22192&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:00 GMT
- PULL 3 | uninum 442397 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=224+S+Main+St%2C+Harrisonburg%2C+VA+22801&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:02 GMT
- PULL 3 | uninum 445564 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=251+W+Lee+Hwy%2C+Warrenton%2C+VA+20186&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:03 GMT
- PULL 3 | uninum 466498 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=4235+Annandale+Rd%2C+Annandale%2C+VA+22003&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:05 GMT
- PULL 3 | uninum 469496 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=410+William+St%2C+Fredericksburg%2C+VA+22401&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:06 GMT
- PULL 3 | uninum 47074 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=200+Peppers+Ferry+Rd%2C+Wytheville%2C+VA+24382&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:08 GMT
- PULL 3 | uninum 481684 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9103+Centreville+Rd%2C+Manassas%2C+VA+20110&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:10 GMT
- PULL 3 | uninum 488794 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=332+Maple+Ave+E%2C+Vienna%2C+VA+22180&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:11 GMT
- PULL 3 | uninum 497232 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9516+Old+Keene+Mill+Rd%2C+Burke%2C+VA+22015&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:13 GMT
- PULL 3 | uninum 497950 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=23+Scenic+Hwy%2C+Churchville%2C+VA+24421&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:15 GMT
- PULL 3 | uninum 508194 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=14122+Lee+Highway%2C+Fairfax%2C+VA+22031&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:16 GMT
- PULL 3 | uninum 517570 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=3030+Clarendon+Blvd%2C+Arlington%2C+VA+22201&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:18 GMT
- PULL 3 | uninum 517927 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=6705+Whittier+Ave%2C+Mclean%2C+VA+22101&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:20 GMT
- PULL 3 | uninum 518473 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=7415+Laughlin+Blvd%2C+Spotsylvania+Courthouse%2C+VA+22553&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:21 GMT
- PULL 3 | uninum 528023 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=4605+Daisy+Reid+Ave%2C+Woodbridge%2C+VA+22192&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:24 GMT
- PULL 3 | uninum 589858 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=4210+Plank+Rd%2C+Fredericksburg%2C+VA+22407&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:26 GMT
- PULL 3 | uninum 625459 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=100+Akers+Farm+Rd%2C+Christiansburg%2C+VA+24073&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:27 GMT
- PULL 3 | uninum 626395 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=12030+Sunrise+Valley+Dr%2C+Reston%2C+VA+20191&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:29 GMT
- PULL 3 | uninum 637091 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=2521+Cowan+Blvd%2C+Fredericksburg%2C+VA+22401&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:31 GMT
- PULL 3 | uninum 638450 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=1821+Michael+Faraday+Dr%2C+Reston%2C+VA+20190&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:32 GMT
- PULL 3 | uninum 661496 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=2065+Huguenot+Road%2C+North+Chesterfield%2C+VA+23235&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:34 GMT
- PULL 3 | uninum 663907 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=9757+Phair+Way%2C+Manassas%2C+VA+20110&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:36 GMT
- PULL 3 | uninum 7397 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=100+S+Fairfax+St%2C+Alexandria%2C+VA+22314&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:37 GMT
- PULL 3 | uninum 74896 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=100+W+Jubal+Early+Dr%2C+Winchester%2C+VA+22601&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:39 GMT
- PULL 3 | uninum 8219 | https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=195++West+Main+Strret%2C+Monterey%2C+VA+24465&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:41 GMT

### PULL 3 flagged-branch excerpts (FDIC record + geocoder first match, as returned)

- PULL 3 | uninum 508194 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "508194", "OFFNAME": "CENTREVILLE BRANCH", "ADDRESS": "14122 Lee Highway", "CITY": "Fairfax", "STALP": "VA", "ZIP": "22031", "STCNTY": "51059", "LATITUDE": "38.860077", "LONGITUDE": "-77.259257"}
```
- PULL 3 | uninum 508194 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"14122 Lee Highway, Fairfax, VA 22031"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 3 | uninum 518473 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "518473", "OFFNAME": "SPOTSYLVANIA COURTHOUSE BRANCH", "ADDRESS": "7415 Laughlin Blvd", "CITY": "Spotsylvania Courthouse", "STALP": "VA", "ZIP": "22553", "STCNTY": "51177", "LATITUDE": "38.205925000000036", "LONGITUDE": "-77.57299499999993"}
```
- PULL 3 | uninum 518473 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"7415 Laughlin Blvd, Spotsylvania Courthouse, VA 22553"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 3 | uninum 663907 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "663907", "OFFNAME": "MANASSAS BRANCH", "ADDRESS": "9757 Phair Way", "CITY": "Manassas", "STALP": "VA", "ZIP": "20110", "STCNTY": "51683", "LATITUDE": "38.7515731", "LONGITUDE": "-77.478839"}
```
- PULL 3 | uninum 663907 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"9757 Phair Way, Manassas, VA 20110"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 3 | uninum 8219 | FDIC record (excerpt, values as returned):
```json
{"UNINUM": "8219", "OFFNAME": "MONTEREY BRANCH", "ADDRESS": "195  West Main Strret", "CITY": "Monterey", "STALP": "VA", "ZIP": "24465", "STCNTY": "51091", "LATITUDE": "38.416626", "LONGITUDE": "-79.559836"}
```
- PULL 3 | uninum 8219 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"195  West Main Strret, Monterey, VA 24465"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[{"tigerLine":{"side":"L","tigerLineId":"172822818"},"geographies":{"Counties":[{"GEOID":"51091","CENTLAT":"+38.3622579","AREAWATER":1791756,"STATE":"51","BASENAME":"Highland","OID":"27590765115510","LSADC":"06","FUNCSTAT":"A","INTPTLAT":"+38.3662431","NAME":"Highland County","OBJECTID":1446,"CENTLON":"-079.5685507","COUNTYCC":"H1","COUNTYNS":"01673774","AREALAND":1075266882,"INTPTLON":"-079.5644718","MTFCC":"G4020","COUNTY":"091"}]},"coordinates":{"x":-79.582632843174,"y":38.413067628384},"addressComponents":{"zip":"24465","streetName":"MAIN","preType":"","city":"MONTEREY","preDirection":"W","suffixDirection":"","fromAddress":"195","state":"VA","suffixType":"ST","toAddress":"299","suffixQualifier":"","preQualifier":""},"matchedAddress":"195 W MAIN ST, MONTEREY, VA, 24465"}]}}
```

## Data files

```synmerco-data
branch-geocode-pull1.csv sha256:5760099ad4b0d593bea2c810856cb96543d3b576b075e367db06b7c69e37c532 bytes:7769 rows:40
branch-geocode-pull2.csv sha256:0865eb7457054c2e8b334f251c88870ff5377eb59b5d2d1898f49c22bb359003 bytes:7697 rows:40
branch-geocode-pull3.csv sha256:5760099ad4b0d593bea2c810856cb96543d3b576b075e367db06b7c69e37c532 bytes:7769 rows:40
```

The three CSVs are attached to escrow esc_21e100923e3747a895409c15 under Rule 25 as data files, one row per branch, sorted by uninum, columns in order: uninum, office name, address, city, zip, stcnty, fdic lat, fdic lon, match, matched address, geo lat, geo lon, geoid, km apart, flags. Each CSV's SHA-256 above equals the SHA-256 verified in escrow for that pull.

## Answer to each requirement

1. Three CSV files attached with exactly the listed columns, one row per key as defined (40 rows each; see Data files below for the SHA-256 of each). No pull failed as a whole: PULL 2 had one failed geocoder request (HTTP 502, uninum 225047), recorded as no match with the error excerpted in the PROOF.
2. Every flagged branch matches its FDIC record and geocoder response in the PROOF above (see PULL 1 / PULL 2 / PULL 3 flagged-branch excerpts).
3. Matches, county checks, distances and flags follow the TASK and agree with the CSVs (see Counts and Flagged branches above; county agreement re-checked: GEOID equals STCNTY for every matched branch).
4. The PLATFORM RECORD shows a PULL 1: note and each later PULL note at least 24 hours after the one before (24h 08m 38s, then 24h 10m 41s; see Counts), each with its CSV's row count and SHA-256 (see Data files); each pull's source time (HTTP Date of its first request, see PROOF) is later than the previous pull's; change counts agree with the CSV files (see Changes).