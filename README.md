# Domain Sales - Dashboard

A free dashboard for domain sellers. Drop in a CSV of your sales to see gross, net and what is
still in progress, for the last 30 days, 90 days, 12 months, this year or all time. Each period is
compared with the one before it.

<img width="1188" height="857" alt="image" src="https://github.com/user-attachments/assets/d8a468c6-e080-4ef8-a7fd-bdb62434f27f" />

**Open it:** https://dotcorner.github.io/domain-sales-dashboard/

**Use it offline:** click **Download** on the page, or save [`index.html`](index.html). Then open
the file in any modern browser. It is one file and needs no install or internet connection.

## Your data stays on your computer

- Your CSV is read inside the browser tab. Nothing is uploaded, and there is no server.
- The page blocks itself from going online (a `default-src 'none'` Content-Security-Policy). It
  makes no requests: no tracking, no analytics, no fonts or scripts from elsewhere.
- It only remembers your preferences in your browser: theme, period, currency and column choices.
  Your sales are never kept.
- It is one readable HTML file. View the source to see exactly what it does.

## What it shows

- **Sales, Gross, Net and Average sale,** each with its change against the period before
- **Gross by week, month or year**
- **Where your sales stand:** paid, lease running, in progress, cancelled
- **Buy now against lease to own**
- **Your largest sales,** and a searchable, sortable list of every sale
- **A warning** when a sale is waiting for your auth code
- **A venue filter,** when your file has several marketplaces
- **An "As of" date,** to look at an older file as it stood then

## Your CSV

**Required columns:** domain, sale date and sale price.

**Optional columns:** net, commission, status, sale type and venue. Without them, the matching
tiles say what to add.

Column names are matched for you. Accepted names include:
- `Domain` or `Name`
- `Sale date`, `Sold Date` or `soldAt`
- `Sale price`, `Gross` or `salePrice`
- `Net`, `Commission`, `Status`, `Sale type` or `Type`, `Venue` or `Marketplace`

If a column can't be matched, **Match your columns** lets you pick it.

**Dates** can be written as `2026-10-08`, `4-Jan-2020`, `Jan 4, 2020` or `03/10/2026`. For
numeric dates, it works out whether the day or the month comes first.

**Amounts** can be written as `US$1,234.50`, `1.234,50 €` or `2500`. The currency is detected
from the column name or the amounts, and can be changed.

There is a CSV template on the page, and **Try with sample data** shows a full dashboard with
made-up names.

**Statuses** follow Afternic's:

| Stage | Statuses |
|---|---|
| Paid | Completed, Lease fully paid |
| Lease running | Paid lease installment |
| Cancelled | Cancelled, left out of every figure |
| In progress | Everything else |

Plain words such as "Paid", "Refunded" or "Pending payout" work too.

## Not affiliated

This is an unofficial community tool. It is not affiliated with, endorsed by or connected to
Afternic, GoDaddy or any other marketplace.

## License

- The dashboard is [MIT](LICENSE).
- The embedded Geist and Geist Mono fonts are © Vercel, under the [SIL Open Font License 1.1](OFL-Geist.txt).
