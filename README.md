**#Description:**

The travelling salesman problem (TSP) asks the following question: "Given a list of cities and the distances between each pair of cities, what is the shortest possible route that visits each city exactly once and returns to the origin city?" It is an NP-hard problem in combinatorial optimization, important in theoretical computer science and operations research.

![image]([[https://external-preview.redd.it/oWu9Rd_ykjnEAfbnDQZkc8aq3eNpgvJdZ2rtExtMTNw.png?auto=webp&s=c87aef08f0e2e1536cb4c28a5c420ae5cf5f2d51]([https://upload.wikimedia.org/wikipedia/commons/2/23/Nearestneighbor.gif)](https://upload.wikimedia.org/wikipedia/commons/2/2b/Bruteforce.gif](https://upload.wikimedia.org/wikipedia/commons/2/23/Nearestneighbor.gif)))

**API**

[https://rapidapi.com/zilinskivan/api/3d-bin-packing-problem/](https://rapidapi.com/zilinskivan/api/travelling-salesman-problem-best-route-finder)

**Body request example:**

<pre>
[
    [
        -33.91999211736843,
        151.26079376999053,
        "Giles Baths, AU"
    ],
    [
        -33.919396335569076,
        151.2604308128357,
        "Bali Memorial, AU"
    ],
    [
        -33.9183457704342,
        151.25914335250854,
        "Dunningham Reserve, AU"
    ],
    [
        -33.91682331831124,
        151.26137495040894,
        "Jesse Shop, AU"
    ],
    [
        -33.92034005252707,
        151.25825822353363,
        "Coogee Beach, AU"
    ]
]
</pre>

**Response (Solution):**

<pre>
{
  "s": 1,
  "route": [
    {
      "direction": "Giles Baths, AU - Bali Memorial, AU",
      "mi.": 0.04612355633669526
    },
    {
      "direction": "Bali Memorial, AU - Jesse Shop, AU",
      "mi.": 0.1858284345685766
    },
    {
      "direction": "Jesse Shop, AU - Dunningham Reserve, AU",
      "mi.": 0.16563294513250845
    },
    {
      "direction": "Dunningham Reserve, AU - Coogee Beach, AU",
      "mi.": 0.14683297404143456
    },
    {
      "direction": "Coogee Beach, AU - Giles Baths, AU",
      "mi.": 0.147342096941222
    }
  ],
  "locations": [
    {
      "latitude": -33.91999211736843,
      "longitude": 151.26079376999053,
      "id": "Giles Baths, AU"
    },
    {
      "latitude": -33.919396335569076,
      "longitude": 151.2604308128357,
      "id": "Bali Memorial, AU"
    },
    {
      "latitude": -33.9183457704342,
      "longitude": 151.25914335250854,
      "id": "Dunningham Reserve, AU"
    },
    {
      "latitude": -33.91682331831124,
      "longitude": 151.26137495040894,
      "id": "Jesse Shop, AU"
    },
    {
      "latitude": -33.92034005252707,
      "longitude": 151.25825822353363,
      "id": "Coogee Beach, AU"
    }
  ]
}
</pre>

**Code Samples:**

**CURL**

<pre>
POST /?units=M HTTP/1.1
Content-Type: application/json
X-Rapidapi-Key: Your API KEY
X-Rapidapi-Host: travelling-salesman-problem-best-route-finder.p.rapidapi.com
Host: travelling-salesman-problem-best-route-finder.p.rapidapi.com
Content-Length: 511

[
    [
        -33.91999211736843,
        151.26079376999053,
        "Giles Baths, AU"
    ],
    [
        -33.919396335569076,
        151.2604308128357,
        "Bali Memorial, AU"
    ],
    [
        -33.9183457704342,
        151.25914335250854,
        "Dunningham Reserve, AU"
    ],
    [
        -33.91682331831124,
        151.26137495040894,
        "Jesse Shop, AU"
    ],
    [
        -33.92034005252707,
        151.25825822353363,
        "Coogee Beach, AU"
    ]
]
</pre>

**Javascript:**

<pre>
const data = JSON.stringify([
	[
		-33.91999211736843,
		151.26079376999053,
		'Giles Baths, AU'
	],
	[
		-33.919396335569076,
		151.2604308128357,
		'Bali Memorial, AU'
	],
	[
		-33.9183457704342,
		151.25914335250854,
		'Dunningham Reserve, AU'
	],
	[
		-33.91682331831124,
		151.26137495040894,
		'Jesse Shop, AU'
	],
	[
		-33.92034005252707,
		151.25825822353363,
		'Coogee Beach, AU'
	]
]);

const xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener('readystatechange', function () {
	if (this.readyState === this.DONE) {
		console.log(this.responseText);
	}
});

xhr.open('POST', 'https://travelling-salesman-problem-best-route-finder.p.rapidapi.com/?units=M');
xhr.setRequestHeader('content-type', 'application/json');
xhr.setRequestHeader('X-RapidAPI-Key', 'Your API KEY');
xhr.setRequestHeader('X-RapidAPI-Host', 'travelling-salesman-problem-best-route-finder.p.rapidapi.com');

xhr.send(data);
</pre>

**NodeJS:**

<pre>
const axios = require('axios');

const options = {
  method: 'POST',
  url: 'https://travelling-salesman-problem-best-route-finder.p.rapidapi.com/',
  params: {units: 'M'},
  headers: {
    'content-type': 'application/json',
    'X-RapidAPI-Key': 'Your API KEY',
    'X-RapidAPI-Host': 'travelling-salesman-problem-best-route-finder.p.rapidapi.com'
  },
  data: [
    [
      -33.91999211736843,
      151.26079376999053,
      'Giles Baths, AU'
    ],
    [
      -33.919396335569076,
      151.2604308128357,
      'Bali Memorial, AU'
    ],
    [
      -33.9183457704342,
      151.25914335250854,
      'Dunningham Reserve, AU'
    ],
    [
      -33.91682331831124,
      151.26137495040894,
      'Jesse Shop, AU'
    ],
    [
      -33.92034005252707,
      151.25825822353363,
      'Coogee Beach, AU'
    ]
  ]
};

try {
	const response = await axios.request(options);
	console.log(response.data);
} catch (error) {
	console.error(error);
}
</pre>

**PHP**

<pre>
<?php

$curl = curl_init();

curl_setopt_array($curl, [
	CURLOPT_URL => "https://travelling-salesman-problem-best-route-finder.p.rapidapi.com/?units=M",
	CURLOPT_RETURNTRANSFER => true,
	CURLOPT_ENCODING => "",
	CURLOPT_MAXREDIRS => 10,
	CURLOPT_TIMEOUT => 30,
	CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
	CURLOPT_CUSTOMREQUEST => "POST",
	CURLOPT_POSTFIELDS => json_encode([
		[
				-33.91999211736843,
				151.26079376999053,
				'Giles Baths, AU'
		],
		[
				-33.919396335569076,
				151.2604308128357,
				'Bali Memorial, AU'
		],
		[
				-33.9183457704342,
				151.25914335250854,
				'Dunningham Reserve, AU'
		],
		[
				-33.91682331831124,
				151.26137495040894,
				'Jesse Shop, AU'
		],
		[
				-33.92034005252707,
				151.25825822353363,
				'Coogee Beach, AU'
		]
	]),
	CURLOPT_HTTPHEADER => [
		"X-RapidAPI-Host: travelling-salesman-problem-best-route-finder.p.rapidapi.com",
		"X-RapidAPI-Key: Your API KEY",
		"content-type: application/json"
	],
]);

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
	echo "cURL Error #:" . $err;
} else {
	echo $response;
}
</pre>
