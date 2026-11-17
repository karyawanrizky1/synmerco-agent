# Branch location data check — Burke & Herbert Bank & Trust Company

Bank: Burke & Herbert Bank & Trust Company, FDIC CERT 11578, Virginia. Job job_2d7a231154ca4170. Escrow esc_21e100923e3747a895409c15 (FUNDED, net $4.75). Seller: Karyawanrizky1 (did:pkh:eip155:8453:0xa12Ed7470708Fc1fb153B19D3dB9e313E36F1ba6).

Task: every Virginia branch of this bank from FDIC BankFind, geocoded with the US Census Geocoder, checked for county agreement (GEOID = STCNTY) and distance (haversine, Earth radius 6,371 km). Flags: no match; county differs; over 1 km apart. Three timed pulls, 24 hours apart, each with its own CSV data file attached under Rule 25.

## Sources and method

- FDIC BankFind, `api.fdic.gov/banks/locations`, filters `CERT:11578 AND STALP:VA`, fields NAME, OFFNAME, UNINUM, ADDRESS, CITY, STALP, ZIP, COUNTY, STCNTY, LATITUDE, LONGITUDE, limit 100, format json. No key.
- US Census Geocoder, `geocoding.geo.census.gov/geocoder/geographies/onelineaddress`, one line ADDRESS, CITY, STALP ZIP; benchmark Public_AR_Current, vintage Current_Current, layers Counties, format json; one request per second. No key. Each PROOF request line below gives the branch address; the full request URL is that endpoint with the address, for example: https://geocoding.geo.census.gov/geocoder/geographies/onelineaddress?address=8736+Cooper+Rd%2C+Alexandria%2C+VA+22309&benchmark=Public_AR_Current&vintage=Current_Current&layers=Counties&format=json.
- Match: yes when the geocoder returns at least one address match; the first match is used. Distance: haversine between the FDIC point and the geocoder point. Figures: 2 decimals, half away from zero, from unrounded values.
- Only the sources listed here were used. No login-only or paid source. No advice, opinions or forecasts beyond what the sources state.

## Counts

| Pull | Branches | Match yes | Match no | Match rate | No match | County differs | Over 1 km |
|---|---|---|---|---|---|---|---|
| PULL 1 | 40 | 37 | 3 | 92.50% | 3 | 0 | 1 |
| PULL 2 | 40 | 36 | 4 | 90.00% | 4 | 0 | 1 |
| PULL 3 | 40 | 37 | 3 | 92.50% | 3 | 0 | 1 |

PULL 1 note: 2026-11-15 05:15:50 UTC. PULL 2 note: 2026-11-16 05:24:28 UTC (24h 08m 38s after PULL 1). PULL 3 note: 2026-11-17 05:35:09 UTC (24h 10m 40s after PULL 2). CORRECTED PULL 1/3 notes (2026-11-17 08:44:31-32 UTC) state the current file for PULL 1 and PULL 3; the CORRECTED PULL 2 note (revision round 4, 2026-11-17 09:15:09 UTC) restates the pull-time PULL 2 file (40 rows, SHA-256 as in Data files). Earliest submit 2026-11-17 03:42:46 UTC; deliver by 2026-11-19 11:42:46 UTC.

## Flagged branches

Every branch with a flag in any pull, with both addresses and the distance. No branch ever had a county-differ flag: for every matched branch in every pull, GEOID equals STCNTY.

### PULL 1 — 4 flagged of 40 branches

- uninum 8219, MONTEREY BRANCH, FDIC: 195  West Main Strret, Monterey, 24465, STCNTY 51091, FDIC (38.416626, -79.559836); match yes; matched: 195 W MAIN ST, MONTEREY, VA, 24465; geocoder (38.413067628384, -79.582632843174), GEOID 51091; 2.03 km apart; flags: over 1 km apart.
- uninum 508194, CENTREVILLE BRANCH, FDIC: 14122 Lee Highway, Fairfax, 22031, STCNTY 51059, FDIC (38.860077, -77.259257); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 518473, SPOTSYLVANIA COURTHOUSE BRANCH, FDIC: 7415 Laughlin Blvd, Spotsylvania Courthouse, 22553, STCNTY 51177, FDIC (38.205925000000036, -77.57299499999993); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 663907, MANASSAS BRANCH, FDIC: 9757 Phair Way, Manassas, 20110, STCNTY 51683, FDIC (38.7515731, -77.478839); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.

### PULL 2 — 5 flagged of 40 branches

- uninum 225047, COOPER ROAD BRANCH, FDIC: 8736 Cooper Rd, Alexandria, 22309, STCNTY 51059, FDIC (38.71964620832338, -77.12453736789736); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 508194, CENTREVILLE BRANCH, FDIC: 14122 Lee Highway, Fairfax, 22031, STCNTY 51059, FDIC (38.860077, -77.259257); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 518473, SPOTSYLVANIA COURTHOUSE BRANCH, FDIC: 7415 Laughlin Blvd, Spotsylvania Courthouse, 22553, STCNTY 51177, FDIC (38.205925000000036, -77.57299499999993); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 663907, MANASSAS BRANCH, FDIC: 9757 Phair Way, Manassas, 20110, STCNTY 51683, FDIC (38.7515731, -77.478839); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 8219, MONTEREY BRANCH, FDIC: 195  West Main Strret, Monterey, 24465, STCNTY 51091, FDIC (38.416626, -79.559836); match yes; matched: 195 W MAIN ST, MONTEREY, VA, 24465; geocoder (38.413067628384, -79.582632843174), GEOID 51091; 2.03 km apart; flags: over 1 km apart.

### PULL 3 — 4 flagged of 40 branches

- uninum 8219, MONTEREY BRANCH, FDIC: 195  West Main Strret, Monterey, 24465, STCNTY 51091, FDIC (38.416626, -79.559836); match yes; matched: 195 W MAIN ST, MONTEREY, VA, 24465; geocoder (38.413067628384, -79.582632843174), GEOID 51091; 2.03 km apart; flags: over 1 km apart.
- uninum 508194, CENTREVILLE BRANCH, FDIC: 14122 Lee Highway, Fairfax, 22031, STCNTY 51059, FDIC (38.860077, -77.259257); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 518473, SPOTSYLVANIA COURTHOUSE BRANCH, FDIC: 7415 Laughlin Blvd, Spotsylvania Courthouse, 22553, STCNTY 51177, FDIC (38.205925000000036, -77.57299499999993); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.
- uninum 663907, MANASSAS BRANCH, FDIC: 9757 Phair Way, Manassas, 20110, STCNTY 51683, FDIC (38.7515731, -77.478839); match no; matched: (none); geocoder (-, -), GEOID -; distance n/a; flags: no match.

## County name per branch

County name per branch, from the geocoder Counties layer (NAME) where matched; FDIC COUNTY where not matched (labelled). CSV columns unchanged.

PULL 1 and PULL 3 (identical): 7397 Alexandria city; 8219 Highland County; 47074 Wythe County; 74896 Winchester city; 212907 Wythe County; 225042 Alexandria city; 225043 Alexandria city; 225044 Fairfax County; 225047 Fairfax County; 225048 Fairfax County; 225049 Fairfax County; 225051 Alexandria city; 225052 Falls Church city; 263661 Tazewell County; 358770 Fairfax County; 360368 Fairfax County; 363744 Loudoun County; 419173 Rockingham County; 429547 Bath County; 432308 Prince William County; 442397 Harrisonburg city; 445564 Fauquier County; 466498 Fairfax County; 469496 Fredericksburg city; 481684 Manassas city; 488794 Fairfax County; 497232 Fairfax County; 497950 Augusta County; 508194 Fairfax (FDIC county); 517570 Arlington County; 517927 Fairfax County; 518473 Spotsylvania (FDIC county); 528023 Prince William County; 589858 Spotsylvania County; 625459 Montgomery County; 626395 Fairfax County; 637091 Fredericksburg city; 638450 Fairfax County; 661496 Chesterfield County; 663907 Manassas City (FDIC county)

PULL 2: 212907 Wythe County; 225042 Alexandria city; 225043 Alexandria city; 225044 Fairfax County; 225047 Fairfax (FDIC county); 225048 Fairfax County; 225049 Fairfax County; 225051 Alexandria city; 225052 Falls Church city; 263661 Tazewell County; 358770 Fairfax County; 360368 Fairfax County; 363744 Loudoun County; 419173 Rockingham County; 429547 Bath County; 432308 Prince William County; 442397 Harrisonburg city; 445564 Fauquier County; 466498 Fairfax County; 469496 Fredericksburg city; 47074 Wythe County; 481684 Manassas city; 488794 Fairfax County; 497232 Fairfax County; 497950 Augusta County; 508194 Fairfax (FDIC county); 517570 Arlington County; 517927 Fairfax County; 518473 Spotsylvania (FDIC county); 528023 Prince William County; 589858 Spotsylvania County; 625459 Montgomery County; 626395 Fairfax County; 637091 Fredericksburg city; 638450 Fairfax County; 661496 Chesterfield County; 663907 Manassas City (FDIC county); 7397 Alexandria city; 74896 Winchester city; 8219 Highland County

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

Every request below is listed with its UTC time (the HTTP Date response header). FDIC excerpts below are the API response lines as returned (re-fetched 2026-11-17 10:05:05 GMT; every field matches the CSVs). FDIC first-request HTTP Date per pull: PULL 1 Sun, 15 Nov 2026 04:43:33 GMT; PULL 2 Mon, 16 Nov 2026 05:21:11 GMT; PULL 3 Tue, 17 Nov 2026 05:31:34 GMT. Each pull's first-request HTTP Date is later than the previous pull's.

### PULL 1 requests

- FDIC: https://api.fdic.gov/banks/locations?filters=CERT%3A11578%20AND%20STALP%3AVA&fields=NAME,OFFNAME,UNINUM,ADDRESS,CITY,STALP,ZIP,COUNTY,STCNTY,LATITUDE,LONGITUDE&limit=100&format=json | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:33 GMT
- PULL 1 | uninum 7397 | 100 S Fairfax St, Alexandria, VA 22314 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:43 GMT
- PULL 1 | uninum 8219 | 195  West Main Strret, Monterey, VA 24465 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:47 GMT
- PULL 1 | uninum 47074 | 200 Peppers Ferry Rd, Wytheville, VA 24382 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:10 GMT
- PULL 1 | uninum 74896 | 100 W Jubal Early Dr, Winchester, VA 22601 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:45 GMT
- PULL 1 | uninum 212907 | 148 Ivanhoe Rd, Max Meadows, VA 24360 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:33 GMT
- PULL 1 | uninum 225042 | 306 E Monroe Ave, Alexandria, VA 22301 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:35 GMT
- PULL 1 | uninum 225043 | 1775 Jamieson Ave, Alexandria, VA 22314 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:37 GMT
- PULL 1 | uninum 225044 | 5731 Telegraph Rd, Alexandria, VA 22303 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:39 GMT
- PULL 1 | uninum 225047 | 8736 Cooper Rd, Alexandria, VA 22309 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:41 GMT
- PULL 1 | uninum 225048 | 5705 Seminary Rd, Falls Church, VA 22041 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:42 GMT
- PULL 1 | uninum 225049 | 2604 Sherwood Hall Ln, Alexandria, VA 22306 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:44 GMT
- PULL 1 | uninum 225051 | 1705 Fern St, Alexandria, VA 22302 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:46 GMT
- PULL 1 | uninum 225052 | 225 W Broad St, Falls Church, VA 22046 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:48 GMT
- PULL 1 | uninum 263661 | 108 Spruce St, Bluefield, VA 24605 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:50 GMT
- PULL 1 | uninum 358770 | 6200 Backlick Rd, Springfield, VA 22150 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:52 GMT
- PULL 1 | uninum 360368 | 6210 Inter Parcel Rd, Alexandria, VA 22315 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:53 GMT
- PULL 1 | uninum 363744 | 204 Catoctin Cir Se, Leesburg, VA 20175 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:55 GMT
- PULL 1 | uninum 419173 | 1925 Stone Spring Rd, Rockingham, VA 22801 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:57 GMT
- PULL 1 | uninum 429547 | 9406 Sam Snead Hwy, Hot Springs, VA 24445 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:43:59 GMT
- PULL 1 | uninum 432308 | 14008 Smoketown Rd, Woodbridge, VA 22192 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:01 GMT
- PULL 1 | uninum 442397 | 224 S Main St, Harrisonburg, VA 22801 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:02 GMT
- PULL 1 | uninum 445564 | 251 W Lee Hwy, Warrenton, VA 20186 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:04 GMT
- PULL 1 | uninum 466498 | 4235 Annandale Rd, Annandale, VA 22003 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:06 GMT
- PULL 1 | uninum 469496 | 410 William St, Fredericksburg, VA 22401 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:08 GMT
- PULL 1 | uninum 481684 | 9103 Centreville Rd, Manassas, VA 20110 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:12 GMT
- PULL 1 | uninum 488794 | 332 Maple Ave E, Vienna, VA 22180 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:14 GMT
- PULL 1 | uninum 497232 | 9516 Old Keene Mill Rd, Burke, VA 22015 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:16 GMT
- PULL 1 | uninum 497950 | 23 Scenic Hwy, Churchville, VA 24421 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:17 GMT
- PULL 1 | uninum 508194 | 14122 Lee Highway, Fairfax, VA 22031 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:19 GMT
- PULL 1 | uninum 517570 | 3030 Clarendon Blvd, Arlington, VA 22201 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:21 GMT
- PULL 1 | uninum 517927 | 6705 Whittier Ave, Mclean, VA 22101 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:23 GMT
- PULL 1 | uninum 518473 | 7415 Laughlin Blvd, Spotsylvania Courthouse, VA 22553 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:25 GMT
- PULL 1 | uninum 528023 | 4605 Daisy Reid Ave, Woodbridge, VA 22192 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:27 GMT
- PULL 1 | uninum 589858 | 4210 Plank Rd, Fredericksburg, VA 22407 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:29 GMT
- PULL 1 | uninum 625459 | 100 Akers Farm Rd, Christiansburg, VA 24073 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:31 GMT
- PULL 1 | uninum 626395 | 12030 Sunrise Valley Dr, Reston, VA 20191 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:33 GMT
- PULL 1 | uninum 637091 | 2521 Cowan Blvd, Fredericksburg, VA 22401 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:35 GMT
- PULL 1 | uninum 638450 | 1821 Michael Faraday Dr, Reston, VA 20190 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:37 GMT
- PULL 1 | uninum 661496 | 2065 Huguenot Road, North Chesterfield, VA 23235 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:39 GMT
- PULL 1 | uninum 663907 | 9757 Phair Way, Manassas, VA 20110 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:41 GMT

### PULL 1 flagged-branch excerpts (FDIC record + geocoder first match, as returned)

- PULL 1 | uninum 8219 | FDIC record (as returned, one line):
```json
{"ZIP":"24465","STCNTY":"51091","OFFNAME":"MONTEREY BRANCH","CITY":"Monterey","LONGITUDE":-79.559836,"ADDRESS":"195  West Main Strret","STALP":"VA","LATITUDE":38.416626,"COUNTY":"Highland","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":8219,"ID":"8219"}
```
- PULL 1 | uninum 8219 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"195  West Main Strret, Monterey, VA 24465"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[{"tigerLine":{"side":"L","tigerLineId":"172822818"},"geographies":{"Counties":[{"GEOID":"51091","CENTLAT":"+38.3622579","AREAWATER":1791756,"STATE":"51","BASENAME":"Highland","OID":"27590765115510","LSADC":"06","FUNCSTAT":"A","INTPTLAT":"+38.3662431","NAME":"Highland County","OBJECTID":1446,"CENTLON":"-079.5685507","COUNTYCC":"H1","COUNTYNS":"01673774","AREALAND":1075266882,"INTPTLON":"-079.5644718","MTFCC":"G4020","COUNTY":"091"}]},"coordinates":{"x":-79.582632843174,"y":38.413067628384},"addressComponents":{"zip":"24465","streetName":"MAIN","preType":"","city":"MONTEREY","preDirection":"W","suffixDirection":"","fromAddress":"195","state":"VA","suffixType":"ST","toAddress":"299","suffixQualifier":"","preQualifier":""},"matchedAddress":"195 W MAIN ST, MONTEREY, VA, 24465"}]}}
```
- PULL 1 | uninum 508194 | FDIC record (as returned, one line):
```json
{"ZIP":"22031","STCNTY":"51059","OFFNAME":"CENTREVILLE BRANCH","CITY":"Fairfax","LONGITUDE":-77.259257,"ADDRESS":"14122 Lee Highway","STALP":"VA","LATITUDE":38.860077,"COUNTY":"Fairfax","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":508194,"ID":"508194"}
```
- PULL 1 | uninum 508194 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"14122 Lee Highway, Fairfax, VA 22031"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 1 | uninum 518473 | FDIC record (as returned, one line):
```json
{"ZIP":"22553","STCNTY":"51177","OFFNAME":"SPOTSYLVANIA COURTHOUSE BRANCH","CITY":"Spotsylvania Courthouse","LONGITUDE":-77.57299499999993,"ADDRESS":"7415 Laughlin Blvd","STALP":"VA","LATITUDE":38.205925000000036,"COUNTY":"Spotsylvania","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":518473,"ID":"518473"}
```
- PULL 1 | uninum 518473 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"7415 Laughlin Blvd, Spotsylvania Courthouse, VA 22553"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 1 | uninum 663907 | FDIC record (as returned, one line):
```json
{"ZIP":"20110","STCNTY":"51683","OFFNAME":"MANASSAS BRANCH","CITY":"Manassas","LONGITUDE":-77.478839,"ADDRESS":"9757 Phair Way","STALP":"VA","LATITUDE":38.7515731,"COUNTY":"Manassas City","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":663907,"ID":"663907"}
```
- PULL 1 | uninum 663907 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"9757 Phair Way, Manassas, VA 20110"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```

### PULL 2 requests

- FDIC: https://api.fdic.gov/banks/locations?filters=CERT%3A11578%20AND%20STALP%3AVA&fields=NAME,OFFNAME,UNINUM,ADDRESS,CITY,STALP,ZIP,COUNTY,STCNTY,LATITUDE,LONGITUDE&limit=100&format=json | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:11 GMT
- PULL 2 | uninum 212907 | 148 Ivanhoe Rd, Max Meadows, VA 24360 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:12 GMT
- PULL 2 | uninum 225042 | 306 E Monroe Ave, Alexandria, VA 22301 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:14 GMT
- PULL 2 | uninum 225043 | 1775 Jamieson Ave, Alexandria, VA 22314 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:16 GMT
- PULL 2 | uninum 225044 | 5731 Telegraph Rd, Alexandria, VA 22303 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:23 GMT
- PULL 2 | uninum 225047 | 8736 Cooper Rd, Alexandria, VA 22309 | status: request failed (HTTP Error 502: ) — no HTTP Date (a failed request has none). Send time (derived, labelled): Mon, 16 Nov 2026 05:21:24 GMT — 1 s after the previous request's response at 05:21:23 GMT; the exact second was not recorded.
- PULL 2 | uninum 225048 | 5705 Seminary Rd, Falls Church, VA 22041 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:46 GMT
- PULL 2 | uninum 225049 | 2604 Sherwood Hall Ln, Alexandria, VA 22306 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:48 GMT
- PULL 2 | uninum 225051 | 1705 Fern St, Alexandria, VA 22302 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:50 GMT
- PULL 2 | uninum 225052 | 225 W Broad St, Falls Church, VA 22046 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:51 GMT
- PULL 2 | uninum 263661 | 108 Spruce St, Bluefield, VA 24605 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:21:53 GMT
- PULL 2 | uninum 358770 | 6200 Backlick Rd, Springfield, VA 22150 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:02 GMT
- PULL 2 | uninum 360368 | 6210 Inter Parcel Rd, Alexandria, VA 22315 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:04 GMT
- PULL 2 | uninum 363744 | 204 Catoctin Cir Se, Leesburg, VA 20175 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:05 GMT
- PULL 2 | uninum 419173 | 1925 Stone Spring Rd, Rockingham, VA 22801 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:13 GMT
- PULL 2 | uninum 429547 | 9406 Sam Snead Hwy, Hot Springs, VA 24445 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:15 GMT
- PULL 2 | uninum 432308 | 14008 Smoketown Rd, Woodbridge, VA 22192 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:17 GMT
- PULL 2 | uninum 442397 | 224 S Main St, Harrisonburg, VA 22801 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:18 GMT
- PULL 2 | uninum 445564 | 251 W Lee Hwy, Warrenton, VA 20186 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:20 GMT
- PULL 2 | uninum 466498 | 4235 Annandale Rd, Annandale, VA 22003 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:22 GMT
- PULL 2 | uninum 469496 | 410 William St, Fredericksburg, VA 22401 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:23 GMT
- PULL 2 | uninum 47074 | 200 Peppers Ferry Rd, Wytheville, VA 24382 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:25 GMT
- PULL 2 | uninum 481684 | 9103 Centreville Rd, Manassas, VA 20110 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:26 GMT
- PULL 2 | uninum 488794 | 332 Maple Ave E, Vienna, VA 22180 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:28 GMT
- PULL 2 | uninum 497232 | 9516 Old Keene Mill Rd, Burke, VA 22015 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:30 GMT
- PULL 2 | uninum 497950 | 23 Scenic Hwy, Churchville, VA 24421 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:31 GMT
- PULL 2 | uninum 508194 | 14122 Lee Highway, Fairfax, VA 22031 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:34 GMT
- PULL 2 | uninum 517570 | 3030 Clarendon Blvd, Arlington, VA 22201 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:36 GMT
- PULL 2 | uninum 517927 | 6705 Whittier Ave, Mclean, VA 22101 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:38 GMT
- PULL 2 | uninum 518473 | 7415 Laughlin Blvd, Spotsylvania Courthouse, VA 22553 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:39 GMT
- PULL 2 | uninum 528023 | 4605 Daisy Reid Ave, Woodbridge, VA 22192 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:41 GMT
- PULL 2 | uninum 589858 | 4210 Plank Rd, Fredericksburg, VA 22407 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:42 GMT
- PULL 2 | uninum 625459 | 100 Akers Farm Rd, Christiansburg, VA 24073 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:44 GMT
- PULL 2 | uninum 626395 | 12030 Sunrise Valley Dr, Reston, VA 20191 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:46 GMT
- PULL 2 | uninum 637091 | 2521 Cowan Blvd, Fredericksburg, VA 22401 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:47 GMT
- PULL 2 | uninum 638450 | 1821 Michael Faraday Dr, Reston, VA 20190 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:49 GMT
- PULL 2 | uninum 661496 | 2065 Huguenot Road, North Chesterfield, VA 23235 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:50 GMT
- PULL 2 | uninum 663907 | 9757 Phair Way, Manassas, VA 20110 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:52 GMT
- PULL 2 | uninum 7397 | 100 S Fairfax St, Alexandria, VA 22314 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:54 GMT
- PULL 2 | uninum 74896 | 100 W Jubal Early Dr, Winchester, VA 22601 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:55 GMT
- PULL 2 | uninum 8219 | 195  West Main Strret, Monterey, VA 24465 | status 200 | HTTP Date: Mon, 16 Nov 2026 05:22:57 GMT

### PULL 2 retry of uninum 225047 (revision round 1) — not PULL 2 data

The original PULL 2 request for this branch failed with HTTP 502. During revision round 1, at the evaluator's instruction, it was retried once (HTTP Date: Tue, 17 Nov 2026 08:24:13 GMT, status 200). That retry is NOT PULL 2 data and is not used for the PULL 2 row, counts or Changes above.

### PULL 2 flagged-branch excerpts (FDIC record + geocoder first match, as returned)

- PULL 2 | uninum 225047 | FDIC record (as returned, one line):
```json
{"ZIP":"22309","STCNTY":"51059","OFFNAME":"COOPER ROAD BRANCH","CITY":"Alexandria","LONGITUDE":-77.12453736789736,"ADDRESS":"8736 Cooper Rd","STALP":"VA","LATITUDE":38.71964620832338,"COUNTY":"Fairfax","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":225047,"ID":"225047"}
```
- PULL 2 | uninum 225047 | Geocoder response (as returned — request failed, no match list):
```
HTTP Error 502: 
```
- PULL 2 | uninum 508194 | FDIC record (as returned, one line):
```json
{"ZIP":"22031","STCNTY":"51059","OFFNAME":"CENTREVILLE BRANCH","CITY":"Fairfax","LONGITUDE":-77.259257,"ADDRESS":"14122 Lee Highway","STALP":"VA","LATITUDE":38.860077,"COUNTY":"Fairfax","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":508194,"ID":"508194"}
```
- PULL 2 | uninum 508194 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"14122 Lee Highway, Fairfax, VA 22031"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 2 | uninum 518473 | FDIC record (as returned, one line):
```json
{"ZIP":"22553","STCNTY":"51177","OFFNAME":"SPOTSYLVANIA COURTHOUSE BRANCH","CITY":"Spotsylvania Courthouse","LONGITUDE":-77.57299499999993,"ADDRESS":"7415 Laughlin Blvd","STALP":"VA","LATITUDE":38.205925000000036,"COUNTY":"Spotsylvania","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":518473,"ID":"518473"}
```
- PULL 2 | uninum 518473 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"7415 Laughlin Blvd, Spotsylvania Courthouse, VA 22553"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 2 | uninum 663907 | FDIC record (as returned, one line):
```json
{"ZIP":"20110","STCNTY":"51683","OFFNAME":"MANASSAS BRANCH","CITY":"Manassas","LONGITUDE":-77.478839,"ADDRESS":"9757 Phair Way","STALP":"VA","LATITUDE":38.7515731,"COUNTY":"Manassas City","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":663907,"ID":"663907"}
```
- PULL 2 | uninum 663907 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"9757 Phair Way, Manassas, VA 20110"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 2 | uninum 8219 | FDIC record (as returned, one line):
```json
{"ZIP":"24465","STCNTY":"51091","OFFNAME":"MONTEREY BRANCH","CITY":"Monterey","LONGITUDE":-79.559836,"ADDRESS":"195  West Main Strret","STALP":"VA","LATITUDE":38.416626,"COUNTY":"Highland","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":8219,"ID":"8219"}
```
- PULL 2 | uninum 8219 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"195  West Main Strret, Monterey, VA 24465"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[{"tigerLine":{"side":"L","tigerLineId":"172822818"},"geographies":{"Counties":[{"GEOID":"51091","CENTLAT":"+38.3622579","AREAWATER":1791756,"STATE":"51","BASENAME":"Highland","OID":"27590765115510","LSADC":"06","FUNCSTAT":"A","INTPTLAT":"+38.3662431","NAME":"Highland County","OBJECTID":1446,"CENTLON":"-079.5685507","COUNTYCC":"H1","COUNTYNS":"01673774","AREALAND":1075266882,"INTPTLON":"-079.5644718","MTFCC":"G4020","COUNTY":"091"}]},"coordinates":{"x":-79.582632843174,"y":38.413067628384},"addressComponents":{"zip":"24465","streetName":"MAIN","preType":"","city":"MONTEREY","preDirection":"W","suffixDirection":"","fromAddress":"195","state":"VA","suffixType":"ST","toAddress":"299","suffixQualifier":"","preQualifier":""},"matchedAddress":"195 W MAIN ST, MONTEREY, VA, 24465"}]}}
```

### PULL 3 requests

- FDIC: https://api.fdic.gov/banks/locations?filters=CERT%3A11578%20AND%20STALP%3AVA&fields=NAME,OFFNAME,UNINUM,ADDRESS,CITY,STALP,ZIP,COUNTY,STCNTY,LATITUDE,LONGITUDE&limit=100&format=json | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:34 GMT
- PULL 3 | uninum 7397 | 100 S Fairfax St, Alexandria, VA 22314 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:37 GMT
- PULL 3 | uninum 8219 | 195  West Main Strret, Monterey, VA 24465 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:41 GMT
- PULL 3 | uninum 47074 | 200 Peppers Ferry Rd, Wytheville, VA 24382 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:08 GMT
- PULL 3 | uninum 74896 | 100 W Jubal Early Dr, Winchester, VA 22601 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:39 GMT
- PULL 3 | uninum 212907 | 148 Ivanhoe Rd, Max Meadows, VA 24360 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:35 GMT
- PULL 3 | uninum 225042 | 306 E Monroe Ave, Alexandria, VA 22301 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:37 GMT
- PULL 3 | uninum 225043 | 1775 Jamieson Ave, Alexandria, VA 22314 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:39 GMT
- PULL 3 | uninum 225044 | 5731 Telegraph Rd, Alexandria, VA 22303 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:40 GMT
- PULL 3 | uninum 225047 | 8736 Cooper Rd, Alexandria, VA 22309 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:42 GMT
- PULL 3 | uninum 225048 | 5705 Seminary Rd, Falls Church, VA 22041 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:43 GMT
- PULL 3 | uninum 225049 | 2604 Sherwood Hall Ln, Alexandria, VA 22306 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:45 GMT
- PULL 3 | uninum 225051 | 1705 Fern St, Alexandria, VA 22302 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:46 GMT
- PULL 3 | uninum 225052 | 225 W Broad St, Falls Church, VA 22046 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:49 GMT
- PULL 3 | uninum 263661 | 108 Spruce St, Bluefield, VA 24605 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:50 GMT
- PULL 3 | uninum 358770 | 6200 Backlick Rd, Springfield, VA 22150 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:52 GMT
- PULL 3 | uninum 360368 | 6210 Inter Parcel Rd, Alexandria, VA 22315 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:53 GMT
- PULL 3 | uninum 363744 | 204 Catoctin Cir Se, Leesburg, VA 20175 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:55 GMT
- PULL 3 | uninum 419173 | 1925 Stone Spring Rd, Rockingham, VA 22801 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:57 GMT
- PULL 3 | uninum 429547 | 9406 Sam Snead Hwy, Hot Springs, VA 24445 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:31:58 GMT
- PULL 3 | uninum 432308 | 14008 Smoketown Rd, Woodbridge, VA 22192 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:00 GMT
- PULL 3 | uninum 442397 | 224 S Main St, Harrisonburg, VA 22801 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:02 GMT
- PULL 3 | uninum 445564 | 251 W Lee Hwy, Warrenton, VA 20186 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:03 GMT
- PULL 3 | uninum 466498 | 4235 Annandale Rd, Annandale, VA 22003 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:05 GMT
- PULL 3 | uninum 469496 | 410 William St, Fredericksburg, VA 22401 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:06 GMT
- PULL 3 | uninum 481684 | 9103 Centreville Rd, Manassas, VA 20110 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:10 GMT
- PULL 3 | uninum 488794 | 332 Maple Ave E, Vienna, VA 22180 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:11 GMT
- PULL 3 | uninum 497232 | 9516 Old Keene Mill Rd, Burke, VA 22015 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:13 GMT
- PULL 3 | uninum 497950 | 23 Scenic Hwy, Churchville, VA 24421 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:15 GMT
- PULL 3 | uninum 508194 | 14122 Lee Highway, Fairfax, VA 22031 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:16 GMT
- PULL 3 | uninum 517570 | 3030 Clarendon Blvd, Arlington, VA 22201 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:18 GMT
- PULL 3 | uninum 517927 | 6705 Whittier Ave, Mclean, VA 22101 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:20 GMT
- PULL 3 | uninum 518473 | 7415 Laughlin Blvd, Spotsylvania Courthouse, VA 22553 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:21 GMT
- PULL 3 | uninum 528023 | 4605 Daisy Reid Ave, Woodbridge, VA 22192 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:24 GMT
- PULL 3 | uninum 589858 | 4210 Plank Rd, Fredericksburg, VA 22407 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:26 GMT
- PULL 3 | uninum 625459 | 100 Akers Farm Rd, Christiansburg, VA 24073 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:27 GMT
- PULL 3 | uninum 626395 | 12030 Sunrise Valley Dr, Reston, VA 20191 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:29 GMT
- PULL 3 | uninum 637091 | 2521 Cowan Blvd, Fredericksburg, VA 22401 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:31 GMT
- PULL 3 | uninum 638450 | 1821 Michael Faraday Dr, Reston, VA 20190 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:32 GMT
- PULL 3 | uninum 661496 | 2065 Huguenot Road, North Chesterfield, VA 23235 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:34 GMT
- PULL 3 | uninum 663907 | 9757 Phair Way, Manassas, VA 20110 | status 200 | HTTP Date: Tue, 17 Nov 2026 05:32:36 GMT

### PULL 3 flagged-branch excerpts (FDIC record + geocoder first match, as returned)

- PULL 3 | uninum 8219 | FDIC record (as returned, one line):
```json
{"ZIP":"24465","STCNTY":"51091","OFFNAME":"MONTEREY BRANCH","CITY":"Monterey","LONGITUDE":-79.559836,"ADDRESS":"195  West Main Strret","STALP":"VA","LATITUDE":38.416626,"COUNTY":"Highland","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":8219,"ID":"8219"}
```
- PULL 3 | uninum 8219 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"195  West Main Strret, Monterey, VA 24465"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[{"tigerLine":{"side":"L","tigerLineId":"172822818"},"geographies":{"Counties":[{"GEOID":"51091","CENTLAT":"+38.3622579","AREAWATER":1791756,"STATE":"51","BASENAME":"Highland","OID":"27590765115510","LSADC":"06","FUNCSTAT":"A","INTPTLAT":"+38.3662431","NAME":"Highland County","OBJECTID":1446,"CENTLON":"-079.5685507","COUNTYCC":"H1","COUNTYNS":"01673774","AREALAND":1075266882,"INTPTLON":"-079.5644718","MTFCC":"G4020","COUNTY":"091"}]},"coordinates":{"x":-79.582632843174,"y":38.413067628384},"addressComponents":{"zip":"24465","streetName":"MAIN","preType":"","city":"MONTEREY","preDirection":"W","suffixDirection":"","fromAddress":"195","state":"VA","suffixType":"ST","toAddress":"299","suffixQualifier":"","preQualifier":""},"matchedAddress":"195 W MAIN ST, MONTEREY, VA, 24465"}]}}
```
- PULL 3 | uninum 508194 | FDIC record (as returned, one line):
```json
{"ZIP":"22031","STCNTY":"51059","OFFNAME":"CENTREVILLE BRANCH","CITY":"Fairfax","LONGITUDE":-77.259257,"ADDRESS":"14122 Lee Highway","STALP":"VA","LATITUDE":38.860077,"COUNTY":"Fairfax","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":508194,"ID":"508194"}
```
- PULL 3 | uninum 508194 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"14122 Lee Highway, Fairfax, VA 22031"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 3 | uninum 518473 | FDIC record (as returned, one line):
```json
{"ZIP":"22553","STCNTY":"51177","OFFNAME":"SPOTSYLVANIA COURTHOUSE BRANCH","CITY":"Spotsylvania Courthouse","LONGITUDE":-77.57299499999993,"ADDRESS":"7415 Laughlin Blvd","STALP":"VA","LATITUDE":38.205925000000036,"COUNTY":"Spotsylvania","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":518473,"ID":"518473"}
```
- PULL 3 | uninum 518473 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"7415 Laughlin Blvd, Spotsylvania Courthouse, VA 22553"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```
- PULL 3 | uninum 663907 | FDIC record (as returned, one line):
```json
{"ZIP":"20110","STCNTY":"51683","OFFNAME":"MANASSAS BRANCH","CITY":"Manassas","LONGITUDE":-77.478839,"ADDRESS":"9757 Phair Way","STALP":"VA","LATITUDE":38.7515731,"COUNTY":"Manassas City","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":663907,"ID":"663907"}
```
- PULL 3 | uninum 663907 | Geocoder first match (excerpt, as returned):
```
{"result":{"input":{"address":{"address":"9757 Phair Way, Manassas, VA 20110"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[]}}
```

## Data files

```synmerco-data
5d964b720c0df97ca3deee88489e624475077c21572b6480bd39a1986bff6051 branch-geocode-pull1.csv
0865eb7457054c2e8b334f251c88870ff5377eb59b5d2d1898f49c22bb359003 branch-geocode-pull2.csv
5d964b720c0df97ca3deee88489e624475077c21572b6480bd39a1986bff6051 branch-geocode-pull3.csv
```

The three CSVs are attached to escrow esc_21e100923e3747a895409c15 under Rule 25 as data files, one row per branch, sorted by numeric uninum, columns in order: uninum, office name, address, city, zip, stcnty, fdic lat, fdic lon, match, matched address, geo lat, geo lon, geoid, km apart, flags. Each CSV's SHA-256 above equals the SHA-256 verified in escrow for that pull.

## Answer to each requirement

1. Three CSV files attached with exactly the listed columns, one row per key as defined (40 rows each; see Data files below for the SHA-256 of each). No pull failed as a whole. PULL 2's single geocoder request (uninum 225047) failed with HTTP 502 at pull time and is recorded as no match, with the error excerpted in the PROOF; the PULL 2 row, counts and Changes follow that pull-time result. During revision round 1, at the evaluator's instruction, that request was retried once (HTTP Date: Tue, 17 Nov 2026 08:24:13 GMT, HTTP 200); the retry is not PULL 2 data and is not used here. The original PULL 2 note (16 Nov) records 36/40 matched, as the pull-time file shows.
2. Every flagged branch matches its FDIC record and geocoder response in the PROOF above (see PULL 1 / PULL 2 / PULL 3 flagged-branch excerpts).
3. Matches, county checks, distances and flags follow the TASK and agree with the CSVs (see Counts and Flagged branches above; county agreement re-checked: GEOID equals STCNTY for every matched branch; county name per branch: see County name per branch above).
4. The PLATFORM RECORD shows a PULL 1: note and each later PULL note at least 24 hours after the one before (24h 08m 38s, then 24h 10m 40s; see Counts), each with its CSV's row count and SHA-256 (see Data files); each pull's source time (HTTP Date of its first request, see PROOF) is later than the previous pull's; change counts agree with the CSV files (see Changes).

## Requirements and proof

Each requirement below, in the job's own words, with the exact excerpt that proves it directly under it. Every excerpt below also appears in its own section above.

A1 — Three CSV files attached with exactly the listed columns, one row per key as defined.
```
5d964b720c0df97ca3deee88489e624475077c21572b6480bd39a1986bff6051 branch-geocode-pull1.csv
```
A2 — Every flagged branch matches its FDIC record and geocoder response in the PROOF.
```json
{"ZIP":"24465","STCNTY":"51091","OFFNAME":"MONTEREY BRANCH","CITY":"Monterey","LONGITUDE":-79.559836,"ADDRESS":"195  West Main Strret","STALP":"VA","LATITUDE":38.416626,"COUNTY":"Highland","NAME":"Burke & Herbert Bank & Trust Company","UNINUM":8219,"ID":"8219"}
```
```
{"result":{"input":{"address":{"address":"195  West Main Strret, Monterey, VA 24465"},"vintage":{"isDefault":true,"id":"4","vintageName":"Current_Current","vintageDescription":"Current Vintage - Current Benchmark"},"benchmark":{"isDefault":true,"benchmarkDescription":"Public Address Ranges - Current Benchmark","id":"4","benchmarkName":"Public_AR_Current"}},"addressMatches":[{"tigerLine":{"side":"L","tigerLineId":"172822818"},"geographies":{"Counties":[{"GEOID":"51091","CENTLAT":"+38.3622579","AREAWATER":1791756,"STATE":"51","BASENAME":"Highland","OID":"27590765115510","LSADC":"06","FUNCSTAT":"A","INTPTLAT":"+38.3662431","NAME":"Highland County","OBJECTID":1446,"CENTLON":"-079.5685507","COUNTYCC":"H1","COUNTYNS":"01673774","AREALAND":1075266882,"INTPTLON":"-079.5644718","MTFCC":"G4020","COUNTY":"091"}]},"coordinates":{"x":-79.582632843174,"y":38.413067628384},"addressComponents":{"zip":"24465","streetName":"MAIN","preType":"","city":"MONTEREY","preDirection":"W","suffixDirection":"","fromAddress":"195","state":"VA","suffixType":"ST","toAddress":"299","suffixQualifier":"","preQualifier":""},"matchedAddress":"195 W MAIN ST, MONTEREY, VA, 24465"}]}}
```
A3 — Matches, county checks, distances and flags follow the TASK and agree with the CSV.
```
| PULL 1 | 40 | 37 | 3 | 92.50% | 3 | 0 | 1 |
```
A4 — PULL notes timed, with row count and SHA-256 as under DATA FILES; source times increasing; change counts agree with CSVs.
```
the CORRECTED PULL 2 note (revision round 4, 2026-11-17 09:15:09 UTC) restates the pull-time PULL 2 file
```
D1 — PROOF lists every request with its UTC time (HTTP Date).
```
- PULL 1 | uninum 8219 | 195  West Main Strret, Monterey, VA 24465 | status 200 | HTTP Date: Sun, 15 Nov 2026 04:44:47 GMT
```
D2 — pull1 CSV: one row per branch, sorted by uninum, key uninum, values as returned or computed.
```
one row per branch, sorted by numeric uninum, columns in order: uninum, office name, address, city, zip, stcnty, fdic lat, fdic lon, match, matched address, geo lat, geo lon, geoid, km apart, flags.
```
D3 — PULL 2 is the same requests again: CSV PULL 2 and its counts are that pull's own results.
```
- PULL 2 | uninum 225047 | 8736 Cooper Rd, Alexandria, VA 22309 | status: request failed (HTTP Error 502: ) — no HTTP Date (a failed request has none). Send time (derived, labelled): Mon, 16 Nov 2026 05:21:24 GMT — 1 s after the previous request's response at 05:21:23 GMT; the exact second was not recorded.
```
D4 — Each pull quotes the HTTP Date response header of its first request.
```
FDIC first-request HTTP Date per pull: PULL 1 Sun, 15 Nov 2026 04:43:33 GMT; PULL 2 Mon, 16 Nov 2026 05:21:11 GMT; PULL 3 Tue, 17 Nov 2026 05:31:34 GMT.
