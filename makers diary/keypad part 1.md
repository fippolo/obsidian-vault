---
created: 2026-03-21
tags:
  - 3d
  - diary
  - electronics
  - keyboard
---
##  11:14
Today i will be working on a esp32-c3 powered keypad since my aliexpress package has arrived with 5 of them, the design is pretty basic with just 9 switches, the controller, a 1 cell bms to handle a 18650, using the battery itself to angle itself.
![[Pasted image 20260321111618.png]]

## 15:03
I finalised the design adding some mounting point for the eventual back cover and soldered the whole system i powered it up and there looks to be no shorts
Let's quickly go over how it works:
The switches are not connected each to a gpio but they are arranged into a matrix where each column and each row are connected together like this
![[Pasted image 20260321150549.png]]
The problem with this is that if you press both (r1,c1) and (r2,c2) both (r1,c2) and (r2,c1) will result as pressed, this is called ghosting, we can avoid this behavior by making the grid on