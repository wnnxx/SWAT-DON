# SWAT-DON

SWAT-DON extends the nitrogen framework of SWAT revision 664 to represent dissolved organic nitrogen (DON) production, transport and transformation across terrestrial and in-stream systems.

## Model processes

- Soil DON production and partitioning.
- DON transport through surface runoff, lateral flow and shallow groundwater.
- In-stream transformations involving DON, particulate organic nitrogen (PON) and algae.
- DON and PON routing through the river network.

## Available materials

- `code.zip`: SWAT-DON source code.
- `Readme_DON module.txt`: descriptions of source code modifications.
- Model data package: available under the Assets section of release v1.0.0.

Download the model data package from:
[SWAT-DON v1.0.0](../../releases/tag/v1.0.0)

## Software information

- Base model: SWAT revision 664.
- Programming language: Fortran.

## Source code modifications

| File | Description |
| --- | --- |
| Modparm.f | Defines DON state variables and parameters for in-stream DON and PON reactions. |
| allocate_parms.f | Allocates DON simulation variables and extends routing and reach-output arrays. |
| virtual.f | Calculates organic nitrogen loads and prepares DON and PON loads for routing. |
| sim_initday.f | Initializes organic nitrogen variables at the beginning of each day. |
| rtout.f | Calculates downstream organic nitrogen loads and summarizes daily and monthly reach outputs. |
| rchday.f | Writes daily DON and PON loads to the reach output file. |
| rchmon.f | Writes monthly DON and PON loads to the reach output file. |
| rchyr.f | Writes annual DON and PON loads to the reach output file. |
| watqual.f | Calculates reach DON and PON concentrations, mixes inflows with stored water, and updates concentrations following in-stream reactions. |
| submon.f | Supports monthly DON output at the subbasin scale, together with virtual.f. |

## Associated manuscript

SWAT-DON: Integrating dissolved organic nitrogen production, transport and transformation into watershed modelling

## Contact

Xinzhong Du: duxinzhong@caas.cn
