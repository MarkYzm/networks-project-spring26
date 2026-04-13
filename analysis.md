# RTT Analysis

## Q1: Highest Inefficiency Ratio

Frankfurt (google.de) had the highest inefficiency ratio for **city**. Despite transatlantic fiber being well-developed, traffic from Somerville to Frankfurt still traverses multiple backbone segments and exchange points across the Atlantic and into Europe, adding significant queuing and routing overhead relative to the short great-circle distance of ~5,900 km.

Including universities, IIT Delhi had the highest overall inefficiency ratio. Unlike the Google targets, IIT Delhi is a real university server accessed through the public internet. Traffic from Somerville to IIT Delhi most likely traverses a transatlantic cable to Europe, then an undersea cable through the Middle East before reaching India, accumulating queuing and propagation delay across multiple ISPs and exchange points. The result is nearly 2,000 ms measured against a theoretical minimum of ~115 ms.

---

## Q2: Closest to Theoretical Minimum

Sydney (google.com.au) was closest **city** to the theoretical minimum in my measurements, with a ratio of approximately 1.0. The Southern Cross Cable provides a well-developed direct trans-Pacific route between the US East Coast and Australia, and Google's CDN places an edge node in Sydney, so packets travel nearly the great-circle path with minimal detours. 

Including Universities, Seoul National University (snu.ac.kr) was closest to the theoretical minimum for all of my measurement. Korea has excellent trans-Pacific fiber connectivity with low-latency routes to the US East Coast, and Seoul National University's well-peered network infrastructure means packets travel a near-optimal path with minimal queuing or detours.

---

## Q3: Why Does a Packet to Lagos Route Through Europe?

Almost all submarine cables connecting West Africa to the rest of the world land in European cities rather than connecting directly to North America.  The fix is investment in direct-path submarine cables and local peering infrastructure, not a software or routing protocol change.
