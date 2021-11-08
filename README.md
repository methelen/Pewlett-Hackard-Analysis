# Pewlett-Hackard-Analysis

## Overview
Pewlett-Hackard requested analysis on the "silver tsunami" as many current employees reach retirement age.

## Results
![image](https://user-images.githubusercontent.com/90434010/140673686-9065100e-a601-4d39-995f-9435fc3656fd.png)

- Senior Staff and Senior Engineers make up 63.8% of the "silver tsunami"
- Engineers make up 50% of the "silver tsunami"

![image](https://user-images.githubusercontent.com/90434010/140674856-07dd8738-eec1-4fe7-a4d2-84fc557a72a2.png)

- There are 748 Engineers in the mentorship grouping
- 

## Summary
There will be 90,398 roles to be filled as current employees reach retirement age. There currently are 1,549 current employees that could mentor the new hires within the company.

Additional analysis to see what titles the retirees currently hold.

```SELECT COUNT(me.emp_no), t.title
FROM ment_elig AS me
LEFT JOIN titles as t
ON me.emp_no = t.emp_no
GROUP BY t.title
ORDER BY t.title
```

![image](https://user-images.githubusercontent.com/90434010/140671753-787d0bcf-1e5e-4350-b1c2-e28f58175fbd.png)

Additional analysis to see what titles the mentorship eligible staff currently hold.

```SELECT COUNT(meel.emp_no), t.title
FROM mentorship_eligibility AS meel
LEFT JOIN titles as t
ON meel.emp_no = t.emp_no
GROUP BY t.title
ORDER BY t.title
```

![image](https://user-images.githubusercontent.com/90434010/140672558-c4ecd1ba-a2d5-4590-a523-bc0805a7dc6b.png)
