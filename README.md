# Cheap Osaka VPS: how low the monthly price really goes, whether the budget tier holds up for China traffic, and when paying yearly beats monthly (with Evoxt's full plan and price table)

Osaka KVM starts at **$9.90/month** for 1 vCPU, 1 GB RAM, 25 GB SSD and 1 TB of transfer on PartVPS's 39-plan Flex line, and the lowest Japan entry a price tracker currently lists is **$16.88/year** for 512 MB in Tokyo. Evoxt sells Japan from **$2.99/month** for 512 MB and **$4.99** for 1 GB, on one price sheet it applies everywhere it operates. The gap between those numbers and the premium Osaka lines ($49.99/month and up) comes down to routing and support, not CPU count, and that is what decides whether a cheap box is a bargain or a mistake.

What follows covers Evoxt's eleven plans and prices, the two very different products both sold as "Osaka", which carrier each one suits, and what the second-year bill looks like.

> **Most readers should take VM-1 at $5.99/month**: 1 core, 2 GB RAM, 20 GB NVMe, 500 GB transfer, weekly offsite backup included. Choose **VM-0.5 at $2.99** only for a proxy hop, a DNS resolver, a monitoring node, or a test box you rebuild often.

👉 [See Evoxt's Japan plans and the price of each tier](https://bit.ly/EvoXt)

## Evoxt plan list and prices

Evoxt publishes one plan ladder instead of per-city pricing, and the Japan page shows the same plan names and figures as the global list. All eleven plans, in USD, billed monthly:

| Plan | vCPU / RAM / NVMe | Transfer | Price | Order |
| --- | --- | --- | --- | --- |
| VM-0.5 | 1 core / 512 MB / 5 GB | 250 GB | $2.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-0.75 | 1 core / 1 GB / 10 GB | 250 GB | $4.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-1 | 1 core / 2 GB / 20 GB | 500 GB | $5.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-1.5 | 2 cores / 2 GB / 20 GB | 500 GB | $6.95/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-2 | 2 cores / 4 GB / 30 GB | 1,000 GB | $11.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-3 | 4 cores / 4 GB / 30 GB | 1,000 GB | $14.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-4 | 4 cores / 8 GB / 60 GB | 2,000 GB | $23.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-6 | 8 cores / 8 GB / 60 GB | 2,000 GB | $29.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-8 | 8 cores / 16 GB / 80 GB | 3,000 GB | $47.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-12 | 16 cores / 16 GB / 80 GB | 3,000 GB | $60.95/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-16 | 16 cores / 32 GB / 100 GB | 5,000 GB | $95.99/mo | [ Deploy](https://bit.ly/EvoXt) |

The spec column hides two things worth knowing. CPU is advertised as up to 6.0 GHz and the actual CPU model is hidden from the panel. Transfer works as an allowance, then throttling, with no overage charge, so a busy month slows you down instead of generating a bill.

Everything outside the plan grid:

- Weekly offsite backup on every VM at no extra cost, including the $2.99 tier
- Extra IPv4 at $3/month; a paid backup plan priced by the VM's storage size
- Prepay from one month up to three years, or park credit on the account and let it settle invoices
- IPv6, a panel-side firewall, cloning, VNC and usage graphs
- Card, PayPal and Bitcoin accepted
- **No hourly billing** and no DDoS protection, per a third-party host profile from August 2026

That hourly point matters for how you compare. PartVPS bills 39 of its 39 Osaka Flex plans by the hour from $0.0136/hr and stops charging when you destroy the machine, which is ideal for a three-day test. Evoxt bills by the month at minimum, so think in months before you deploy.

## What a cheap Osaka VPS actually is

Almost every budget Osaka listing resolves to the same building: **Equinix OS1, 1-26-1 Shinmachi, Nishi-ku, Osaka 550-0013**. V.PS runs KVM servers there on AS4785 with IIJ as upstream and peering at BBIX Osaka, from €6.95/month for its Cloud KVM line and €8.95/month for Edge, each with 1 IPv4 and 1 IPv6.

BandwagonHost runs two separate Osaka products out of that address, and the difference between them is the single most useful fact in this market:

- **JPOS_1** sits on the E-Commerce tier, upstream Softbank (AS17676) alongside Equinix IX, Google, Cloudflare and NTT. This is the older Osaka node.
- **JPOS_6** sits on the Ultra tier and adds China Telecom CN2 GIA / CTGNet (AS4809 / AS23764) on top of the same IX mix, paired with Unicom AS10099 and Mobile CMIN2 (AS58807) on the return path.

Both are KVM, both use the in-house panel, both are self-managed, and the order pages look nearly identical. The line name is what separates them: E-Commerce means Softbank, Ultra means CN2 GIA. BandwagonHost's own price ladder shows the size of the jump. Plan 1 with 2 cores, 2 GB RAM, 40 GB SSD, 500 GB transfer and a 1.5 Gbps port is **$49.99/month or $499.99/year**, and Plan 3 at 6 cores, 8 GB, 160 GB and 2 TB runs **$165.99/month or $1,665.99/year**.

So the honest picture of "cheap" in Osaka: $9.90 to €8.95 is the Softbank/IIJ neighbourhood, and $49.99 and up is the CN2 GIA neighbourhood. Same city, same building, roughly five times the price. If a listing says Osaka and quotes $10, it is not selling you the premium route.

One more trap. Some results for "Osaka VPS" are not root-access KVM at all. Lilder's Osaka product, for instance, is cPanel with CloudLinux and LiteSpeed on top, aimed at site owners who want a control panel rather than a shell, and its pricing is not comparable to a bare VM.

## Where Evoxt sits on that ladder

Evoxt competes on price per gigabyte of RAM and on included extras rather than on China routing. A tracker that lists the $2.99 plan against every Evoxt location shows the same monthly figure everywhere, which is unusual. Most providers charge a Japan or Hong Kong premium. Here the 1 GB plan is **$4.99** against PartVPS's **$9.90** for the same 1 GB, with a quarter of the transfer (250 GB versus 1 TB) and a smaller disk (10 GB versus 25 GB).

The third-party benchmark grades are worth reading before you buy the smallest tier. On vpsbenchmarks trials, VM-1 at $5.99 scored B for web performance, **E for raw CPU capacity**, C for stability, B for disk I/O and D for network. VM-2 at $11.99 scored C, D, E, B, C on the same axes, and VM-4 at $23.99 scored B for web performance and B for raw CPU. Read that as: the cheap tiers handle a light site or a tunnel fine, and they are not where you put a build job or a database under load.

👉 [Open the Evoxt plan list and check the Japan location before you pay](https://bit.ly/EvoXt)

## Which carrier are your users on?

These recommendations come from a vendor-side writeup on the two BandwagonHost Osaka lines. No independent test has reproduced its packet-loss and latency figures, so treat the direction as a starting point and test from your own network.

- **China Telecom users are the majority of your traffic:** CN2 GIA is the route that holds up at peak. It costs five times the budget tier, and it does nothing for a badly configured web server.
- **China Unicom:** Softbank is often the faster path and always the cheaper one, because the Unicom path via Softbank is short. CN2 GIA tends to be steadier in the evening.
- **China Mobile:** the Ultra line's CN2 GIA plus CMIN2 combination is the safer pick.
- **No mainland audience:** either works. Softbank is usually a little cheaper, and on Evoxt's single price sheet the location choice does not change the bill.

Test before committing. V.PS publishes a public looking glass for its Osaka network with ping, traceroute and speed tests, which is the cheapest way to find out what a route does from your city at 21:00.

## The second-year bill

Monthly list price is the least interesting number in this market. Three verified behaviours:

**PartVPS renews at the price you ordered at.** Its Osaka page states that every plan renews at the figure you ordered it at, and there is no setup fee. A $9.90 plan is $118.80 in year one and $118.80 in year two.

**BandwagonHost's yearly rate is a standing discount, not a coupon.** Plan 1 at $499.99/year against 12 × $49.99 = $599.88 saves about $99.89, or roughly 17%. That is the normal yearly price, so the saving repeats as long as you keep paying yearly.

**Evoxt has no annual discount.** Its monthly prices multiply out to the annual figures third-party trackers list: $2.99 × 12 = $35.88, $4.99 × 12 = $59.88. Prepaying up to three years is available, but the price page publishes no multi-year discount, so prepay for budgeting convenience, not for a lower rate.

A like-for-like comparison at the 1 GB mark, first year and second year:

|  | Monthly | Year one | Year two |
| --- | --- | --- | --- |
| Evoxt VM-0.75 (1 GB / 250 GB) | $4.99 | $59.88 | $59.88 |
| PartVPS C1-1-25 (1 GB / 1 TB) | $9.90 | $118.80 | $118.80 |
| BandwagonHost Osaka Plan 1 (2 GB, CN2 GIA) | $49.99 | $499.99 | $499.99 |

👉 [Start on VM-1 at $5.99/month if you are unsure which size you need](https://bit.ly/EvoXt)

## Who should not buy the $2.99 tier

Skip the bottom of any Osaka price list if any of these apply.

You need someone else to administer the server. Every provider named here is self-managed, BandwagonHost included. Support keeps the network and hardware running; the OS is yours.

You need a written SLA. BandwagonHost's 99.99% SLA applies to its USCA_5 location, not Osaka. V.PS advertises 99.9% on its Osaka line. Evoxt's published material does not offer an SLA on the plans above.

You need more than 5 TB of monthly transfer. Evoxt's ceiling is 5,000 GB on VM-16. Above that you are throttled, not billed, which is fine for a website and wrong for a media mirror.

You need hourly billing for a short experiment. PartVPS's $0.0136/hr model suits a two-day test better than any monthly plan.

Your audience is entirely in Europe or North America. Osaka adds latency for them and buys nothing.

## Five checks before you pay

1. **Read the product line, not the city.** "Osaka" appears on both the Softbank and CN2 GIA products at BandwagonHost. Confirm which tier you are on before checkout.
2. **Confirm the location in the deploy selector.** Evoxt sells Japan among its locations at one price, and the plan ladder is the same everywhere. If Osaka specifically matters for latency, verify the node in the selector rather than assuming it from the country name.
3. **Match transfer to egress.** 250 GB covers a text site. Daily backups or video push past it quickly.
4. **Ask about the refund window in writing before prepaying multiple years.** V.PS offers 14 calendar days on VPS products with exceptions; Lilder offers 30 days on its managed plans. Get Evoxt's terms from support before you commit three years of credit.
5. **Assume self-managed.** Budget for your own time on patching, or for a managed host at several times the price.

## FAQ

**Can a cheap Osaka VPS run a website?**
Yes. A 2 GB plan with 20 GB of disk and a weekly offsite backup handles a small WordPress or Ghost site, a static site, or a Node API comfortably. The limit is CPU headroom on the entry tiers, not the ability to serve pages.

**Is CN2 GIA necessary?**
Only if a large share of your visitors are on China Telecom and evening stability is the thing you are paying for. It costs around five times a Softbank-tier plan. If your traffic is mixed or mostly outside China, the premium buys little.

**Can I stop after one month?**
On Evoxt, yes, monthly billing exists alongside prepaid terms up to three years, but there is no hourly meter. On PartVPS's Osaka Flex line you can go hourly and stop the meter by destroying the machine.

**Will the renewal price jump?**
PartVPS states plainly that plans renew at the ordered figure. Evoxt's monthly price multiplied by twelve matches the annual figures listed publicly, so there is no visible first-year-only discount to expire. Check the cart total before paying anyway, since promotional credit and coupons can change what the first invoice looks like.

**Can I move the server to another city later?**
BandwagonHost's Ultra plans include free datacenter migration to Hong Kong, Tokyo, Singapore, Los Angeles and Amsterdam from inside the panel. Evoxt's panel exposes cloning and plan upgrades. Location migration is not documented in what I checked, so ask support before you build around it.

## Picking from here

A static site, a proxy hop, a DNS box or a monitoring node: **VM-0.5 at $2.99** or **VM-0.75 at $4.99**, and do not pay for cores you will not use.

A small production site or app with real visitors, some of them in China: **VM-1 at $5.99** or **VM-2 at $11.99**, then measure the route from your users' networks. If evening latency on China Telecom turns out to be the problem, no amount of RAM fixes it and you are shopping for a CN2 GIA line at $49.99 and up.

Before you click deploy, confirm two things in the cart: the location shown in the order, and the billing term. Those two fields, not the plan name, determine what you actually get and what you pay next year.

👉 [Compare the $2.99 and $5.99 Evoxt tiers side by side](https://bit.ly/EvoXt)
