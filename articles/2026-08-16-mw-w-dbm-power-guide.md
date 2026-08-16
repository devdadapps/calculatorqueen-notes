---
title: "mW, W, and dBm Are Not the Same: A Practical Device-Power Guide"
date: 2026-08-16
description: "How to convert milliwatts and watts correctly, avoid the mW/MW case trap, and recognize when dBm or energy requires a different calculation."
---

# mW, W, and dBm Are Not the Same

Small electronic devices are often rated in milliwatts, while power supplies and system budgets are usually expressed in watts. Moving between the two is simple—but only if the quantity is linear power and the unit symbols are read exactly.

The SI prefix **milli** means $10^{-3}$, so:

$$
1\ \text{mW} = 0.001\ \text{W}
$$

and therefore:

$$
1000\ \text{mW} = 1\ \text{W}
$$

## The two conversion formulas

To convert milliwatts to watts:

$$
P_{\text{W}} = \frac{P_{\text{mW}}}{1000}
$$

To convert watts to milliwatts:

$$
P_{\text{mW}} = 1000P_{\text{W}}
$$

### Example 1: 250 mW to watts

$$
250 \div 1000 = 0.25
$$

Therefore:

$$
250\ \text{mW} = 0.25\ \text{W}
$$

A result of 250 W would be one thousand times too large.

### Example 2: 5 W to milliwatts

$$
5 \times 1000 = 5000
$$

Therefore:

$$
5\ \text{W} = 5000\ \text{mW}
$$

## A component power-budget example

Suppose a design uses 40 identical modules rated at 75 mW each.

Keep the values in their original unit while adding the load:

$$
40 \times 75\ \text{mW} = 3000\ \text{mW}
$$

Then convert the total:

$$
3000\ \text{mW} \div 1000 = 3\ \text{W}
$$

The combined linear power is 3 W.

This arithmetic is valid only when the ratings describe compatible operating conditions. Idle, typical, transmit, startup, and maximum power may refer to different states. A unit conversion cannot decide which states occur simultaneously.

## Letter case changes the unit

SI symbols are case-sensitive:

- `mW` means milliwatt.
- `MW` means megawatt.
- `W` means watt.

The lowercase `m` represents $10^{-3}$, while uppercase `M` represents $10^{6}$. Consequently:

$$
1\ \text{MW} = 10^6\ \text{W} = 10^9\ \text{mW}
$$

One megawatt is one billion milliwatts. Changing `mW` to `MW` is therefore not a harmless formatting edit.

Standard SI writing also places a space between the number and unit symbol: write `250 mW`, not `250mW`.

## dBm is logarithmic, not another spelling of mW

A value in dBm is a logarithmic power ratio referenced to 1 mW. For positive linear power:

$$
P_{\text{dBm}} =
10\log_{10}\left(\frac{P_{\text{mW}}}{1\ \text{mW}}\right)
$$

When the numeric input is expressed in milliwatts, this is commonly written as:

$$
P_{\text{dBm}} = 10\log_{10}(P_{\text{mW}})
$$

The reverse relationship is:

$$
P_{\text{mW}} = 10^{P_{\text{dBm}}/10}
$$

For example:

$$
20\ \text{dBm} = 100\ \text{mW} = 0.1\ \text{W}
$$

and:

$$
30\ \text{dBm} = 1000\ \text{mW} = 1\ \text{W}
$$

A negative dBm value does not mean negative physical power. It means the positive power is below the 1 mW reference. Zero linear power cannot be converted to a finite dBm value because the logarithm of zero is undefined.

## Power is not energy

Watts and milliwatts measure power—the rate of energy transfer. Watt-hours and milliwatt-hours measure energy accumulated over time.

If a device draws a constant 100 mW for 3 hours:

$$
E = Pt
$$

$$
E = 100\ \text{mW} \times 3\ \text{h}
  = 300\ \text{mWh}
  = 0.3\ \text{Wh}
$$

A direct mW-to-W conversion does not estimate battery runtime, changing load, efficiency loss, or stored energy.

## When a direct converter is appropriate

Use a linear mW/W conversion when:

- the source quantity is non-negative real power;
- the unit is genuinely mW or W;
- no logarithmic dBm conversion is required;
- apparent power in VA is not being substituted for watts;
- voltage, current, efficiency, runtime, and uncertainty do not need to be inferred.

For a quick linear conversion and a visible equality check, I use my own [CalculatorQueen Milliwatt Calculator](https://calculatorqueen.com/calculators/milliwatt-calculator). It converts mW and W without treating dBm, VA, or energy as interchangeable quantities.

> **Ownership disclosure:** I maintain CalculatorQueen. The linked calculator is my own tool, not an independent third-party recommendation.

## Practical checklist

Before accepting a result, check that:

1. `mW` has not been accidentally changed to `MW`.
2. The conversion direction matches the formula.
3. Component ratings represent compatible operating states.
4. Intermediate values were not rounded before aggregation.
5. The original specification describes real power rather than dBm, VA, or energy.

## References

- [BIPM: SI Prefixes](https://www.bipm.org/en/measurement-units/si-prefixes)
- [BIPM: The International System of Units](https://www.bipm.org/en/publications/si-brochure)
- [NIST: Writing with SI Units](https://www.nist.gov/pml/owm/writing-si-metric-system-units)
