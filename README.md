# LeanSearch v2 UCLA Server



## Quick Start


LeanSearch-v2 Standard Mode is deployed at `http://131.179.184.52:8000`


1. This server address is on UCLA’s internal network. **Please connect to the campus network or UCLA VPN before accessing it.**


2. Standard mode API call:
```
curl -X POST http://131.179.184.52:8000/search \
  -H 'Content-Type: application/json' \
  -d '{"query": ["the order of a group element divides the order of the group"], "num_results": 10}'
```

3. For Reasoning mode, since it is based on Standard mode with some additional processing using Claude Sonnet 4.5, you can follow the [LeanSearch-v2](https://github.com/frenzymath/LeanSearch-v2) repository to run it. (Note that Reasoning mode seems much slower than Standard mode)