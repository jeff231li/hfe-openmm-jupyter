# HFE calculation with OpenMM

This repository contain examples of running hydration free energy (HFE) in OpenMM. The notebook calculates the HFE for ethanol in TIP3P waterbox with GAFF force field parameters. The calculation of HFE (or <img src="https://render.githubusercontent.com/render/math?math=\Delta G_{solv}">), is split into the electrostatic and van der Waals (vdW) contributions:

<img src="https://render.githubusercontent.com/render/math?math=\Delta G_{solv} = \Delta G_{elec} %2B \Delta G_{vdw}">

The vdW interaction between ethanol and the solvent is decoupled while the electrostatics are annihilated. Thus <img src="https://render.githubusercontent.com/render/math?math=\Delta G_{elec}"> requires an extra calculation in vacuum

<img src="https://render.githubusercontent.com/render/math?math=\Delta G_{elec} = \Delta G_{elec}^{bulk} %2D \Delta G_{elec}^{vacuum}">

The final HFE are:
 * <img src="https://render.githubusercontent.com/render/math?math=\Delta G_{elec}^{vacuum} = -2.35 kcal/mol">
 * <img src="https://render.githubusercontent.com/render/math?math=\Delta G_{elec}^{bulk} = -7.52 kcal/mol">
 * <img src="https://render.githubusercontent.com/render/math?math=\Delta G_{vdw} = 1.78 kcal/mol">
 * <img src="https://render.githubusercontent.com/render/math?math=\Delta G_{solv} = -3.39 kcal/mol">
