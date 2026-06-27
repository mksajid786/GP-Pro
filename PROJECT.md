# GP Pro

## Overview

GP Pro is a professional TradingView Pine Script indicator for
discretionary futures and crypto trading.

It combines: - Trend Following - Smart Money Concepts (SMC) - Market
Structure - Multi Timeframe Analysis - Liquidity Concepts -
Institutional Scoring - Trade Planning

This project is developed as production software.

Current Stable Version: GP Pro 4.0B

Current Development Branch: GP Pro 5.0-dev

------------------------------------------------------------------------

# Primary Goal

Create one professional indicator that helps traders answer only one
question:

"Should I trade now?"

Every feature must improve decision quality.

Never add features simply because they look impressive.

------------------------------------------------------------------------

# Design Philosophy

Professional • Minimal • Fast • Reliable • No repaint • Low chart
clutter • Institutional logic

------------------------------------------------------------------------

# Coding Standards

-   Use Pine Script Version 6.
-   No duplicated calculations.
-   Functions should be reusable.
-   Avoid deeply nested logic.
-   Keep calculations separated into engines.
-   Every engine must be independent.
-   Use descriptive variable names.
-   Never break existing features unless replacing them with a better
    implementation.

------------------------------------------------------------------------

# Project Architecture

-   Core Engine
-   Trend Engine
-   Structure Engine
-   Liquidity Engine
-   FVG Engine
-   Order Block Engine
-   Decision Engine
-   Trade Engine
-   Dashboard Engine
-   Alert Engine

Each engine should have clearly separated code blocks.

------------------------------------------------------------------------

# Dashboard Philosophy

Dashboard should help traders make decisions in under 3 seconds.

Show only important information.

Avoid unnecessary colors.

Use colors only when they communicate meaning.

Dashboard order: 1. Trend 2. MTF 3. Structure 4. Liquidity 5. FVG 6. OB
7. Premium / Discount 8. RSI 9. Volume 10. Score 11. Confidence 12. Bias
13. Action 14. Setup 15. Trade Plan

------------------------------------------------------------------------

# Decision Engine

Weighted score.

Maximum score: 100.

Scores above 90 should be rare.

-   90--100: Perfect Institutional Setup
-   80--89: High Probability
-   70--79: Good Setup
-   60--69: Acceptable
-   Below 60: No Trade unless exceptional context.

------------------------------------------------------------------------

# Smart Money Rules

-   Never repaint.
-   Always use confirmed pivots.
-   Only nearest active Order Block.
-   Only nearest active Fair Value Gap.
-   Clean filled zones automatically.

------------------------------------------------------------------------

# Trade Engine

Provide: - Entry - Stop Loss - TP1 - TP2 - Risk Reward - Trade
direction - Confidence

No automatic trading. Only decision support.

------------------------------------------------------------------------

# Dashboard Colors

-   Dark background
-   Neutral rows remain gray
-   Only color rows that represent actionable information

Green = Bullish

Red = Bearish

Yellow = Neutral

Orange = Waiting

Blue = Information

Purple = Special SMC information

------------------------------------------------------------------------

# Development Rules

-   Small commits.
-   Each commit must compile.
-   Every commit should improve either:
    -   Performance
    -   Readability
    -   Decision Quality
-   Never all three at once.

------------------------------------------------------------------------

# Branch Strategy

-   main → Stable releases
-   dev → Active development

------------------------------------------------------------------------

# Version Roadmap

-   5.0-dev → Architecture rewrite
-   5.0-beta → Feature complete
-   5.0-rc → Performance optimization
-   5.0 → Production release

------------------------------------------------------------------------

# Developer Notes

This project has evolved through versions 1.x to 4.0B.

Do not remove proven functionality.

Refactor before adding features.

Maintain backward compatibility whenever possible.

The codebase should become easier to maintain with every commit.

Quality is preferred over speed.
