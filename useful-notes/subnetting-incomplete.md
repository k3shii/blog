# Subnetting (incomplete)

## IPV4 Subnetting Calculation



### Step 1: Classified subnet and usable host

Normal subnet is /24 which equal to subnet mask of 255.255.255.0

To calculate host you need to count from behind

```
// The subnet given is /27, how many is the host?

By using binary reprensetation caounting from behind shows that the octet is 6
So calculate with 2^5 = 
```

To calculate subnet you need to count from the back

```
// The s
```

<table><thead><tr><th width="110">Subnet</th><th>/25</th><th>/26</th><th>/27</th><th>/28</th><th>/29</th><th>/30</th><th>/31</th><th>/32</th></tr></thead><tbody><tr><td>Octet</td><td>8</td><td>7</td><td>6</td><td>5</td><td>4</td><td>3</td><td>2</td><td>1</td></tr><tr><td>Subnet Mask</td><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td><td>1</td></tr><tr><td>Host</td><td>256</td><td>128</td><td>64</td><td>32</td><td>16</td><td>8</td><td>4</td><td>2</td></tr><tr><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>

Maximum subnet is /32 which equal to subnet mask of 255.255.255.255

To calculate usable host

/27 is given as the subnet and calculate the host by&#x20;

Usable host = Total host - Subnet ID - Broadcast ID

Example:

/24

Subnet mask = 255.255.255.0

Usable host = 254



/25

Subnet mask = 255.255.255.

<table><thead><tr><th width="180">Subnet ID</th><th width="414" align="center">Usable host range</th><th>Broadcast ID</th></tr></thead><tbody><tr><td></td><td align="center"></td><td></td></tr><tr><td></td><td align="center"></td><td></td></tr><tr><td></td><td align="center"></td><td></td></tr><tr><td></td><td align="center"></td><td></td></tr></tbody></table>
