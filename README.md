# -A-THREE-STEP-FRAMEWORK-for-UNDERWATER-IMAGE-RESTORATION
A Three-Step Framework for Underwater Image Restoration

This repository presents a three-step image restoration framework designed to address the complex degradation present in underwater environments. Underwater images suffer from turbidity, color distortion, non-uniform illumination, motion blur, and noise, which cannot be effectively handled by a single restoration technique. To address this, the proposed framework decomposes the restoration process into physically and perceptually motivated stages, combining classical image processing with modern generative modeling.

Step 1: Contrast Enhancement and Illumination Normalization

The first stage focuses on correcting low contrast and uneven illumination, which are common due to light absorption and scattering in water. Contrast enhancement techniques are applied to normalize intensity distributions and improve visibility of structural details. This step prepares the image for learning-based restoration by reducing extreme illumination variations that negatively affect model convergence.

Step 2: Adaptive Color Correction

Underwater images often exhibit strong color casts caused by wavelength-dependent light attenuation. In this step, adaptive color correction is applied to compensate for color imbalance and restore perceptual realism. The method dynamically adjusts color channels based on scene statistics rather than relying on fixed assumptions, allowing it to generalize across different water conditions.

Step 3: Diffusion-Based Restoration

The final stage employs a U-Net–based diffusion model to progressively remove residual noise, turbidity artifacts, and motion blur. Instead of directly mapping degraded images to clean outputs, the diffusion framework learns the noise distribution and its variance across timesteps, enabling stable restoration under highly noisy and uncertain conditions. This probabilistic formulation allows the model to handle dynamic noise patterns commonly found in underwater imagery.

Key Features

Modular three-stage pipeline combining classical and deep learning methods

Explicit modeling of underwater noise using diffusion processes

Robust to turbidity, motion blur, uneven illumination, and color distortion

Designed for real-world underwater data with imperfect ground truth

Applications

Underwater robotics and autonomous vehicles

Marine biology and habitat monitoring

Underwater surveillance and inspection

Preprocessing for downstream computer vision tasks (detection, tracking, mapping)

Related Publication

This work is based on the following publication:

F. Iqbal and B. U. Töreyin, Underwater Turbid Image Restoration Using Diffusion Models,
33rd Signal Processing and Communications Applications Conference (SIU), 2025.
