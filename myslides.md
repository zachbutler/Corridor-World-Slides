---
author: Zach Butler, Shalini Kusuru, Markus Schultz, Reddi Babu Gundugallu
title: Corridor World
date: November 15, 2018
---

# original method
```java
public double calcReward() {
    double newReward = 0;
    
    if ((mx==chx)&&(my==chy)) {
        mousescore++;
        newReward += cheeseReward;
    }
		
    if ((cx==mx) && (cy==my)) {
        catscore++;
        newReward -= deathPenalty;
    }
		
    return newReward;
		
}
```

# original results
![Original](originalCorridors.png)\

# revised method
```java
public double calcReward() {

*
*
*
    if ((mx != cx) && (my != cy) && (mx != chx) && (my != chy)) {
        newReward += 10;
    }

    return newReward;
```

# revised results
![Revised](revCorridors.png)\
