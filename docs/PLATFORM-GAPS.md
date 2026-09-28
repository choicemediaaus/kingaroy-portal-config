# Platform gaps

Things Kingaroy needs that the platform can't do through configuration.
Each is built in the platform as a feature every client gets, never as a
Kingaroy special case.

Format: what · why Kingaroy needs it · scope section · status (open /
scheduled in the platform / done).

## Confirmed gaps

From Kingaroy's operations feedback, 2026-09-28. All were added to the
platform scope on 2026-09-28 as tracked changes, waiting for Kate to
accept. Status: **proposed in scope**.

| # | What | Why Kingaroy needs it | Scope section |
|---|---|---|---|
| G1 | Goods-in scanning of supplier garment barcodes against the PO; count on screen for items with no barcode | Stock checked in accurately; hats have no barcode | §7.12, §8 |
| G2 | Pack-out verification: each garment scanned into its carton, record kept | Stops "we didn't receive it" disputes (JB's Wear swing tags scan) | §7.12, §8 |
| G3 | Multi-step decoration per garment (e.g. screen print then embroidery; DTF) | Kingaroy runs emb, DTF, screen print and combinations | §7.12 |
| G4 | Subcontracted decoration: PO to outside decorator with only the relevant lines, approved artwork PDF attached, overdue flag after N days | Bulk embroidery goes to a larger embroiderer | §7.12, §8 |
| G5 | Packing slips/job tickets as A4, 2-up A4 or 6×4 label | A4 slips waste paper; label printer | §7.12 |
| G6 | Returns and size swaps: numbered RA with barcode, customer-paid freight invoiced and paid before replacement ships, tracked to close | Current size-swap RA process, made accountable | §7.16 (new), §7.13 |
| G7 | Returned-stock register for resaleable returns (not faulty goods) | Everything in the warehouse accounted for | §7.16, §8, §13 |

Kingaroy's own settings for these (data, not code): overdue flag after
10 days for subcontracted work; 6×4 labels; customer pays return freight
and pays the outbound freight invoice before the replacement ships.

**Scope decision for Kate:** G7 is a limited stock register, and §13
currently puts stock control out of scope. The tracked change carves out
returned stock only. The feedback's wider "everything in the warehouse
accounted for" would be full stock control, which is still out of scope.

## Candidates, waiting on the client

docs/PORTAL-OPTIONS.md lists 11 options that the scope (10 Sep 2026)
didn't cover. All 11 were added to the platform scope on 2026-09-28 as
tracked changes (§7.2, §7.6, §7.7; wrong-size swaps under §7.16). Any that Kingaroy's
completed getting-started workbook shows it actually needs get moved up
into "Confirmed gaps" with the reason.
