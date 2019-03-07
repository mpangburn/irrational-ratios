# Irrational Ratios in Insulin Therapy

## Background

Traditional insulin therapy for individuals with diabetes defines three ratios in describing insulin needs:

1. The basal rate $$B(t)​$$, which describes the insulin necessary per hour to keep blood glucose stable in the absence of carbohydrates.
2. The insulin sensitivity factor $$ISF(t)​$$, which describes the drop in blood glucose concentration per unit of delivered insulin.
3. The insulin-to-carbohydrate ratio $$ICR(t)$$, which describes the insulin necessary for the body to absorb one gram of carbohydrate.

These ratios are functions of time to account for variability over the course of a day. In the following example, we use constant functions to simplify computations. Consider the following (contrived) ratios:

$$B(t) = 1 \: U/h​$$

$$ISF(t) = {30 \: mg/dL/U}​$$

$$ICR(t) = 15 \: g/U^{*}$$

An individual using these ratios:
1. Requires one unit of insulin per hour to maintain stable blood glucose values.
2. Sees a 30 milligrams per deciliter drop in blood glucose for every unit of insulin delivered.
3. Requires one unit of insulin for every fifteen grams of carbohydrate consumed.

---

$$^*$$The name 'insulin-to-carbohydrate ratio' implies units of $$U/g$$. In practice, however, its reciprocal lends itself to more convenient mental math in computing mealtime insulin doses. A person living with diabetes often estimates carbohydrates in multiples of ten or fifteen grams.

## Developing Intuition

Individuals with diabetes are educated to associate each of these ratios with a distinct need for insulin:

- The basal rate covers baseline insulin needs over the course of the day.
- The insulin sensitivity factor is used in insulin dosing calculations for correcting hyperglycemia.
- The insulin-to-carbohydrate ratio is used in insulin dosing calculations at mealtime.

In all of these cases, however, insulin serves the same purpose: to enable the cells of the body to absorb glucose from the bloodstream. So, why use three different ratios to describe the body's response to insulin? With some simple dimensional analysis, we derive new relationships:

$$1) \: B(t) \times ISF(t) = 1 \: U/h \times 30 \: mg/dL/U = 30 \: mg/dL/h​$$

$$2) \: \frac{ISF(t)}{ICR(t)} = \frac{30 \: mg/dL/U}{15 \: g/U} = 2 \: mg/dL/g​$$

Multiplying the basal rate with the insulin sensitivity factor (1) yields a value whose unit indicates an hourly change in blood glucose. Dividing the insulin sensitivity factor by the insulin-to-carbohydrate ratio (2) yields a value whose unit indicates a change in blood glucose per gram of carbohydrate.

Indeed, the units here suffice to tell the story: the first value describes the body's natural production of glucose. It has a name: endogenous glucose production, $$EGP(t)$$. The second value describes the increase in blood glucose per gram of carbohydrate consumed, henceforth referred to as the carbohydrate sensitivity factor, $$CSF(t)^†$$.

$$EGP(t) = B(t) \times ISF(t)​$$

$$CSF(t) = \frac{ISF(t)}{ICR(t)}$$

In context, these values mean the following:
1. Every hour, the individual's natural bodily processes elevate their blood glucose by 30 milligrams per deciliter.
2. For every gram of carbohydrate the individual consumes, digestion yields a two milligram per deciliter increase in blood glucose.

These ratios describe intuitive physiological processes: the body produces glucose regularly to aid in the prevention of hypoglycemia, and every gram of carbohydrate corresponds to an increase in blood glucose concentration when digested.

Derived from the original set of ratios (basal rate, insulin sensitivity factor, and insulin-to-carbohydrate ratio), this new set of ratios (hourly endogenous glucose production, insulin sensitivity factor, and carbohydrate sensitivity factor) encodes identical information for use in insulin therapy, yet requires only one ratio to describe the body's response to insulin.

---

$$^†$$A reviewing endocrinologist noted that the abbreviation CSF is already present in medical jargon to refer to cerebrospinal fluid. If of concern, the term glucose-to-carbohydrate ratio (GCR) encapsulates the same meaning.

## Getting Sensitive

Changes in insulin sensitivity are a common phenomenon encountered by individuals living with diabetes. Fluctuating hormones, illness, and exercise—among other conditions—can have sudden effects on the body's reception of insulin.

To account for a change in insulin sensitivity with the derived set of ratios, the necessary change is apparent: the insulin sensitivity factor must be adjusted. If a particular increase in insulin resistance results in a thirty percent increase in insulin needs, the adjusted ratios are as follows:

$$EGP(t) = 30 \: mg/dL/h \:$$ (unchanged)

$$ISF(t) = \frac{30 \: mg/dL/U}{130\%} \approx 23 \: mg/dL/U​$$

$$CSF(t) = 2 \: mg/dL/g \:$$ (unchanged)

This adjusted set of ratios reads clearly: the increase in insulin resistance has not affected the body's regular production of glucose nor the body's absorption of glucose from digested carbohydrates. The increase in insulin resistance implies that the same amount of insulin yields a reduced effect on blood glucose.

How would this change in sensitivity affect the original set of ratios? Applying the same change to the insulin sensitivity factor results in the following:

$$B(t) = 1 \: U/h​$$

$$ISF(t) = \frac{30 \: mg/dL/U}{130\%} \approx 23 \: mg/dL/U​$$

$$ICR(t) = 15 \: g/U​$$

The flaw quickly becomes evident: if insulin resistance has increased, why have the baseline and mealtime insulin amounts remained unchanged? A quick conversion to the other set of ratios makes apparent the true effects of this adjustment:

$$EGP(t) = B(t) \times ISF(t) = 1 \: U/h \times 23 \: mg/dL/U = 23 \: mg/dL/h$$

$$CSF(t) = \frac{ISF(t)}{ICR(t)} = \frac{23 \: mg/dL/U}{15 \: g/U} \approx 1.5 \: mg/dL/g​$$

In holding the basal rate and insulin-to-carbohydrate ratios fixed, this change in insulin sensitivity factor produced implicit, unintended side effects; namely, endogenous glucose production and carbohydrate sensitivity both decreased.

Properly accounting for this increase insulin resistance using the traditional set of ratios is more involved. The relative change must be applied to each ratio individually in order to achieve the same effect:

$$B(t) = 1 \: U/h \times 130\% = 1.3 \: U/h $$

$$ISF(t) = \frac{30 \: mg/dL/U}{130\%} \approx 23 \: mg/dL/U​$$

$$ICR(t) = \frac{15 \: g/U}{130\%} \approx 11.5 \: g/U$$

Upshot: when using traditional ratios, changing only the _insulin sensitivity_ factor to account for a change in _insulin sensitivity_ is not only insufficient for adjusting treatment, but its silent side effects imply unintuitive biological phenomena.

## Conclusion

The traditional, intertwined set of ratios used in insulin therapy poorly accommodates changes in insulin sensitivity. Describing insulin needs via endogenous glucose production and carbohydrate sensitivity rather than basal insulin rates and insulin-to-carbohydrate ratios results in a set of ratios that maps one-to-one with intuitive physiological processes, avoiding the need to entangle insulin sensitivity across ratios.

---

© [Michael Pangburn](https://twitter.com/pangburnout). March 2019.