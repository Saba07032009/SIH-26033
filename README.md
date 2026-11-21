# Smart India Hackathon Workshop
# Date:21-11-2026
## Reference Number:26018193
## Name:Sabarathinam S

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

## Problem Creater's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Expected Solution: Create a digital marketplace that:

• Connects farmers/FPOs directly with consumers and bulk buyers.
• Provides logistics support.
• Uses AI for demand forecasting and route optimization.

Benefits:

• Better prices for farmers.
• Lower prices for consumers.
• Reduced supply chain inefficiencies.

## Proposed Solution
Our Idea: is a direct farm-to-buyer marketplace that connects smallholder growers straight to local food processors (pickle, pulp, spice, flour, and snack makers), neighborhood fruit/veg vendors, and retail shoppers—eliminating 3–4 layers of mandi commission agents and middlemen.

How It Fixes the Problem:

Dual-Grade Harvest Splitting: Automatically splits a farmer's harvest at the source—sending top-grade produce to retail vendors/consumers and ripe/surplus produce directly to food processors at fair prices instead of letting it rot.

Transparent Floor-Price Shield: Pulls daily mandi rates from and Agmarknet to set a guaranteed minimum farm-gate price so buyers never underpay farmers.

Shared Village Milk-Runs: Combines crates from neighboring farms onto a single scheduled mini-truck, cutting per-farmer transport costs by up to 40%.

What Makes Us Different:

Ripeness-Based Smart Matching: Matches crop ripeness levels with buyer distance—sending firm produce to distant city retailers and peak-ripe produce to nearby food processors.

Street-Vendor Digital Cart: Lets pushcart and neighborhood stall vendors pre-book next-morning crates directly from farms, lowering everyday consumer prices in local markets.

One-Tap Regional Audio Cards: Uses simple visual crop icons + regional voice prompts so farmers with low literacy can list harvests in under 30 seconds.

## Technical Approach
Tech Stack:

Frontend: React Native (Farmer & Driver mobile app with offline caching) + Astro / Tailwind CSS (ultra-fast web portal for food processors, street-vendor unions & bulk buyers).

Backend & Database: Ruby on Rails + Sidekiq (background job queues for batch matching & payouts) + PostgreSQL + ClickHouse (real-time analytics on regional price & supply trends).

AI & Routing:

Demand Forecasting: Amazon DeepAR (probabilistic autoregressive RNN) trained on seasonal crop arrival cycles, local festival demand, and food-processor production schedules.

Route Optimization: jsprit (Java open-source vehicle routing toolkit) solving multi-depot pickup-and-delivery routes with crop-ripeness time windows.

Payments & Interoperability: RazorpayX / UPI Auto-Split Escrow + ONDC Seller Node integration for wider buyer discovery.

How It Works (Flow):

List & Grade: Farmer selects crop icon, enters crate count, and notes ripeness (Firm / Ripe) via voice/app.

AI Split-Match: DeepAR predicts local demand and routes firm crates to retail/street vendors and ripe crates to nearby food processors.

Milk-Run Dispatch: jsprit maps a single multi-farm pickup loop for a local mini-truck with strict freshness deadlines.

Handover & Instant Pay: Buyer scans the crate QR code on arrival; escrow releases instant UPI payouts to the farmer and driver.

<img width="620" height="294" alt="image" src="https://github.com/user-attachments/assets/173e5afa-04a7-4f2b-9a8d-cc19c7839e92" />


## Feasibility and Viability
Why It Works:

Zero Unsold Surplus: Pairing retail buyers with food processors guarantees a buyer for every ripeness stage of a farmer's harvest.

Asset-Light Execution: Uses existing village collection points and local commercial mini-trucks—no expensive warehouses or fleet purchases needed.

Clear Revenue Model: 0% commission for farmers; sustained via a 2% transaction fee charged to food processors and wholesale buyers + a ₹15/crate logistics facilitation fee.

Challenges & Our Fixes:

Crate Weight or Count Disputes: Fix: Standardized returnable plastic crates with tamper-evident QR zip-ties weighed at farm pickup.

Low Smartphone Usage: Fix: Village youth champions (Gram Sahayaks) earn a small per-crate incentive for onboarding and listing harvests for elderly neighbors.

Last-Minute Buyer Cancellations: Fix: Upfront 100% escrow lock upon order confirmation protects farmers from sudden cancellations after harvest.

## Impact and Benefits
Direct Impact:

Farmers: Increase net earnings by 20–28% by selling 100% of their harvest directly to retail and processing buyers without broker cuts.

Consumers & Local Vendors: Lower everyday fruit and vegetable prices by 10–15% at neighborhood stalls and retail stores.

Food Processors: Cut raw-material procurement costs by 15% while securing fresh, traceable farm inputs.

Key Benefits:

Economic: Eliminates middleman commissions, turns surplus ripe crops into steady farmer income, and strengthens local micro-food businesses.

Social: Empowers small farmers and neighborhood street vendors with equal access to fair, transparent digital trade.

Environmental: Routing ripe produce to local processors prevents massive post-harvest dumping, while consolidated milk-runs cut rural diesel emissions

## Research and References
Government Reports & Public Platforms:

1. Ministry of Food Processing Industries (MoFPI) – PM Formalisation of Micro Food Processing Enterprises (PMFME) Scheme

https://www.mofpi.gov.in/schemes/pmfme

2. e-NAM (National Agriculture Market) – Live Mandi Commodity Price Information

https://www.enam.gov.in/web/dashboard/live_price

3. Open Network for Digital Commerce (ONDC) – Official Technical Documentation and Protocol Specifications

https://github.com/ONDC-Official/ONDC-Protocol-Specs

Official website: https://ondc.org
Technical & Academic Sources


4. Salinas, D., Flunkert, V., & Gasthaus, J. (2020). DeepAR: Probabilistic Forecasting with Autoregressive Recurrent Networks. International Journal of Forecasting, 36(3), 1181–1191.

https://doi.org/10.1016/j.ijforecast.2019.07.001

5. jsprit Routing Toolkit – Open-Source Java Vehicle Routing and Pickup-Delivery Solver

https://github.com/graphhopper/jsprit
