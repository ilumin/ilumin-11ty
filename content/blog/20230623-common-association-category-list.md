---
title: Common Association Category List
description: เรารู้ได้ไงว่าควรจะสร้าง association อะไรใน OOP
date: 2023-06-23
tags:
  - OOP
  - OOAD
---

> คำถาม: เรารู้ได้ไงว่าควรจะสร้าง association อะไรใน OOP  
> คำตอบ:
>
> 1. อ้างอิงจาก Common Association Category List ของ Craig Larman
> 2. อ้างอิงจาก Streamlined Object Modeling ของ Peter Coad

## Common Association Category List

เสนอโดย Craig Larman ในหนังสือ "Applying UML and Patterns"[^ref1]

เค้าแบ่ง category ของ class ที่เราน่าจะเอามาพิจารณาสร้างได้ดังนี้

- A is a physical part of B
  - Drawer — Register
  - Wing — Airplane
- A is a logical part of B
  - SalesLineItem — Sale
  - FlightLeg — FlightRoute
- A is physically contained in/on B
  - Register — Store
  - Item — Shelf
  - Passenger — Airplane
- A is logically contained in B
  - ItemDescription — Catalog
  - Flight — FlightSchedule
- A is description for B
  - ItemDescription — Item
  - FlightDescription — Flight
- A is a line item of a transaction or report B
  - SalesLineItem — Sale
  - MaintenanceJob — MaintenanceLog
- A is know/logged/recorded/reported/capture in B
  - Sale — Register
  - Reservation — FlightManifest
- A is a member of B
  - Cashier — Store
  - Pilot — Airline
- A is an organizational subunit of B
  - Department — Store
  - Maintenance — Airline
- A uses or manages B
  - Cashier — Register
  - Pilot — Airplane
- A communicates with B
  - Customer — Cashier
  - Reservation Agent — Passenger
- A is related to a transaction B
  - Customer — Payment
  - Passenger — Ticket
- A is a transaction related to another transaction B
  - Payment — Sale
  - Reservation — Cancellation
- A is next to B
  - SalesLineItem — SalesLineItem
  - City — City
- A is owned by B
  - Register — Store
  - Plane — Airline
- A is an event related to B
  - Sale — Customer
  - Sale — Store
  - Departure — Slight

ซึ่งตัวที่เค้าเน้นคือ

- physical part
- logical part
- physically contained
- logically contained
- recorded

## Though

- มีอะไรมาให้อ้างอิงก็ดีกว่านั่งคิดเอง
- มันเป็น pattern ไม่ได้มีเหตุผลในการทำ association เหมือน Streamlined Object Modeling ของ Coad

[^ref1]: Craig Larman, "Applying UML and Patterns"
