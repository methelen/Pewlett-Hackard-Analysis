# Pewlett-Hackard-Analysis

## Overview
Pewlett-Hackard requested analysis on the "silver tsunami" as many current employees reach retirement age.

## Results
- 
- 
- 
- 

## Summary
There will be x roles to be filled as currnet employees retire from Pewlett-Hackard. There currently are x current employees that could mentor the new hires within the company.

Additional analysis to see what titles the retirees currently hold.
'''
SELECT COUNT(me.emp_no), t.title
FROM ment_elig AS me
LEFT JOIN titles as t
ON me.emp_no = t.emp_no
GROUP BY t.title
ORDER BY t.title
'''

![image](https://user-images.githubusercontent.com/90434010/140671753-787d0bcf-1e5e-4350-b1c2-e28f58175fbd.png)

Additional analysis to see what titles the mentorship eligible staff currently hold.
'''
SELECT COUNT(meel.emp_no), t.title
FROM mentorship_eligibility AS meel
LEFT JOIN titles as t
ON meel.emp_no = t.emp_no
GROUP BY t.title
ORDER BY t.title
'''

![image](https://user-images.githubusercontent.com/90434010/140672558-c4ecd1ba-a2d5-4590-a523-bc0805a7dc6b.png)
