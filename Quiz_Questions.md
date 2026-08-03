# Quiz Questions

Questions to assess participant comprehension of the key learning objectives from
the *Reducing your Climate Impact when Training ML Models* tutorial.

## Q1 Identify sources of emissions

What are the main components for computing-related carbon footprint according to Luccioni's Carbon Emissions Estimation Framework?

<ol type="a">
    <li>Operational emissions come from manufacturing the GPU, while embodied emissions come from electricity used during training.</li>
    <li>Operational emissions come from electricity used during training and inference, while embodied emissions come from manufacturing the hardware itself.</li>
    <li>Both components are driven solely by the number of GPUs used.</li>
    <li>Operational emissions are fixed at purchase time, while embodied emissions grow with each training run.</li>
</ol>

Correct answer: b) Operational = electricity during data processing/training/inference (E × I); embodied = manufacturing hardware, amortized over lifespan.

## Q2 Strategies for reducing model training emissions

Which of the following strategies did the tutorial demonstrate for reducing operational emissions?

<ol type="a">
    <li>Using a simpler algorithm</li>
    <li>Reducing model size</li>
    <li>Applying early stopping when validation loss plateaus</li>
    <li>Hyperparameter optimization</li>
</ol>

Correct answer: all of the above.

## Q3 Measure emissions + approximations

Is the following statement true or false?

CodeCarbon computes emissions as `energy consumed × grid carbon intensity` using the facility's actual Power Usage Effectiveness (PUE) and thus the reported emissions are exact measurements rather than approximations.

Correct answer: FALSE. The notebook emphasizes CodeCarbon's simplifying assumptions (static historical averages, no real-time grid data, no facility-level PUE) make the results approximations, not exact measurements.

## Q4 Reporting emissions in model cards

Why is it recommended to record emissions (e.g., `co2_eq_emissions`) in a model card's YAML front-matter?

<ol type="a">
    <li>Model cards are required by law for all ML models.</li>
    <li>It provides structured, machine-readable disclosure of a model's environmental footprint, including source, hardware used, and geographical location.</li>
    <li>It guarantees the model was trained with zero carbon emissions.</li>
    <li>It replaces the need to actually track emissions during training.</li>
</ol>

Correct answer: b) Structured emissions metadata (emissions, source, training type, geo location, hardware) in model cards enables transparent, parseable reporting.
