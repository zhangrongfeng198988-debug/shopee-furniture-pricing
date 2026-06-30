---
name: shopee-furniture-pricing
description: Build Shopee furniture category pricing-control, product portfolio, promotion-pricing, inventory-feedback, and operator-execution workflows. Use when Codex is asked to plan, audit, simulate, or document ecommerce operations for Shopee furniture, including 引流款/利润款/平销款/新品/清仓 tagging, SKU price ladders, activity discounts, ROAS/fee linkage, inventory pressure, and weekly pricing reviews.
---

# Shopee Furniture Pricing

## Core Intent

Use this skill to turn Shopee furniture operations into a disciplined pricing-control workflow: define each product's role, design price and profit ladders, execute timely series-level adjustments, track sales/cost/inventory feedback, and convert the result into an action plan.

When detailed thresholds, definitions, or checklists are needed, read `references/pricing-framework.md`.

## Default Workflow

1. Identify the task type:
   - **New product pricing**: assign 引流款/利润款/平销款/新品 role, set baseline price, and create SKU profit ladder.
   - **Price-change review**: evaluate urgency, series impact, total real profit, competitor movement, and inventory pressure.
   - **Promotion pricing**: set activity discount by real-receipt margin band, lock-price risk, and SKU participation mix.
   - **Portfolio audit**: check GMV mix, profit-product share, traffic-product overdependence, and aging inventory.
   - **Weekly ops review**: summarize pricing changes, daily sales movement, ROAS/fee usage, inventory changes, and next actions.

2. Ask for or infer the minimum data:
   - product series, SKU list, current prices, proposed prices
   - control tag, product age, real-receipt margin or real profit per SKU
   - daily sales before/after, ROAS, ad spend, GMV, inventory, turnover days
   - competitor prices, activity lock rules, platform submission thresholds

3. Classify the product role before recommending price:
   - 引流款: market hot item or price-sensitive item used to capture traffic and market share.
   - 利润款: differentiated item with pricing power and net-profit contribution.
   - 平销款: stable long-tail item that protects category completeness and risk balance.
   - 新品: main SKU created within 6 months; use pricing to test daily-sales peak and reorder speed.
   - 清仓/灭款: no further purchase plan; price for cash recovery and inventory release.

4. Prefer total real profit over isolated margin rate:
   - Calculate or estimate `sales volume * real profit per unit`.
   - A lower margin can be acceptable when it increases series sales and total real profit.
   - Avoid optimizing one SKU while damaging adjacent SKUs in the same series.

5. Produce an operator-ready output:
   - conclusion: approve, reject, test, or monitor
   - product role and strategic goal
   - exact price/SKU actions
   - expected effect on sales, profit, ROAS, and inventory
   - risks and fallback triggers
   - owner cadence: manager pricing decision, junior partner execution, daily/3-day validation, inventory feedback, next adjustment

## Pricing Rules Of Thumb

- Use a baseline profit floor such as 26% when the user does not provide a different internal target.
- For 利润款, usually price above the assessment baseline by about 8-15% when differentiation supports it.
- For 平销款, usually float above the assessment baseline by about 5-8%.
- For 引流款, follow competitive market pricing, but keep a self-owned system so traffic sacrifice feeds profit-product ammunition.
- Build series ladders by **profit gradient**, not only price tiers. Different sizes and carton/sea-freight costs may break simple price-step logic.
- Use small or demand-size SKUs to create value perception; use larger, differentiated, or non-demand-size SKUs for higher profit contribution.

## Adjustment Discipline

For any price change, check three principles:

1. **Timeliness**: delayed pricing can reduce conversion, monthly sales, future output, and fee efficiency.
2. **Series linkage**: adjust the full SKU ladder when one competitive SKU changes, so value perception stays coherent.
3. **Real-profit response**: simulate total real profit, not just single-SKU margin.

Recommended approval flow:

`urgency/risk assessment -> full-series impact check -> total real-profit simulation -> execution -> daily tracking -> inventory feedback -> next adjustment`

## Promotion Pricing

Balance participation rate, discount setting, and lock-price risk.

- Ensure activity SKU participation is rich enough: include representative traffic, profit, and stable SKUs.
- Set discounts by real-receipt margin:
  - below 20%: about 2%
  - 20-40%: about 3-4%
  - above 40%: about 5%
- Before lock price, leave room for competitor moves and define escalation triggers.

## Review Output Templates

Use these concise formats unless the user asks for another artifact.

### Price-Change Memo

```markdown
结论：
产品角色：
调价动作：
系列影响：
真实利润额测算：
费用/ROAS联动：
库存影响：
风险：
执行与复盘节奏：
```

### Weekly Portfolio Review

```markdown
本周结构：
关键调价：
销售反馈：
费用反馈：
库存反馈：
异常SKU：
下周动作：
需要管理者决策：
```

## Detailed Reference

Read `references/pricing-framework.md` when the task needs:

- precise tag definitions and KPIs
- product-role decision criteria
- activity discount thresholds
- tracking indicators
- inventory/personnel closed-loop workflow
- examples for series-level SKU impact checks
