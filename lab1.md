# Formula 1
## 1 Description
* This project will store and display information related to Formula 1 racing, including different seasons, races within those seasons, and the championships (WDC & WCC) for each season.

* It will provide data on the races for each season, the drivers and constructors involved, and who won the championships.

## 2 Identifying Entities, Attributes, and Relationships:


| Entity          | Attributes                                                                                                                              |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Season**        | `season_id`, `season_year`    |
| **Race**        | `race_id`, `race_name`, `race_date`, `season_id (foreign key)`                    |
| **Driver**     | `driver_id`, `name`, `nationality`                       |
| **Constructor** | `constructor_id`, `name`, `nationality`    |
| **WDC**        | `wdc_id`, `season_id`, `driver_id`, `points`                        |
| **WCC**        | `wcc_id`, `season_id`, `amount`, `constructor_id`, `points`                            |



Relationships:
Season has many Races: A season can have many races (one-to-many).
Race involves many Drivers: A race can have many drivers (many-to-many).
Driver participates in many Races: A driver can participate in multiple races (many-to-many).
Season has one WDC: Each season has one WDC (one-to-one).
Season has one WCC: Each season has one WCC (one-to-one).
Constructor participates in many Races: A constructor can participate in multiple races (many-to-many).

