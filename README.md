# comp120_assignment3

COMP120_versioncontrol

## Project overview

This project is part of COMP120 Assignment 3. It uses GitHub to manage issues, milestones, version control, and collaboration.

# Café Inventory Tracker

The Café Inventory Tracker is a planned Python command-line application that helps café staff record stock counts and see what needs to be reordered before the next delivery. It is designed for stock checks at the end of a shift and count updates when supplies arrive.

## Planned features

- **View inventory** with the current quantity, unit, and reorder level for each item.
- **Update stock counts** after a stock check or delivery. Counts must be whole numbers of zero or more.
- **View a restock list** showing items whose quantity is at or below their reorder level.
- **Save inventory to CSV** and load the saved counts when the program opens again.

## Example stock check

| Item | Quantity | Unit | Reorder level | Status |
| --- | ---: | --- | ---: | --- |
| Oat milk | 2 | cartons | 3 | Restock |
| Espresso beans | 6 | bags | 2 | In stock |
| Takeaway cups | 1 | sleeve | 1 | Restock |

After entering these sample counts, a staff member can open the restock list and see oat milk and takeaway cups. The cups appear because their count is exactly at the reorder level.

## Planned usage

1. Open the program and choose **View inventory**.
2. Choose **Update stock**, select an item, and enter the quantity counted.
3. Choose **View restock list** to see what needs to be reordered.
4. Close the program and reopen it to see the saved counts.

## Testing plan

| Test | Expected result |
| --- | --- |
| Change oat milk from 5 cartons to 2 | The inventory shows 2 cartons and oat milk appears on the restock list. |
| Set takeaway cups to their reorder level of 1 sleeve | Takeaway cups appear on the restock list. |
| Set espresso beans to 0 bags | The program accepts the count and flags espresso beans for restock. |
| Enter `-1`, `2.5`, or `abc` as a count | The program rejects the input and keeps the previous count. |
| Update a count, close the program, and reopen it | The updated count loads from the CSV file. |

## Project status

The first version is in the planning stage. It will use Python 3 and Python's built-in `csv` module. The sample counts above are for demonstrating and testing the planned features.
