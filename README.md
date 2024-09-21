# Technology
All technology files for the open source EDA tools reside in this repository

## Download
- ``git clone https://github.com/silicon-vlsi-org/eda-technology``

## MOSIS Scalable CMOS ([SCMOS]/scn4m_subm)
[SCMOS] is a *lambda-based* scalable design rules that can be interfaced to many CMOS fabrication process available at MOSIS. **NOTE** The scalable design rules does not interface with Fabs now because of lot unique process nuances.

- The Spice model files are located at `<INSTALL-DIR>/eda-technology/scn4m_subm/models/scn4m_cnrs_bsim3v1.lib`
- Typical MOS parameters:
  - **NMOS**: tox=7.6nm, nch=1.7e17/cm^3, Vt0=0.49V, un(mobility)=445 cm^2/Vs
  - **PMOS**: tox=7.6nm, nch=1.7e17/cm^3, Vt0=-0.66V, up(mobility)=151 cm^2/Vs
  - Vdd=5V, Lmin=0.4um, Wmin=0.6um

## Skywater 130nm PDK

- https://www.github.com/google/skywater-pdk
- https://skywater-pdk.readthedocs.io/

- Best way to get the PDK compiled is to clone one of efabless templates and run `make setup`
  - https://github.com/efabless/caravel_user_project
  - https://github.com/efabless/caravel_user_project_analog
- It's installed using a tool called `volare` maintained under the efabless repo:
  - https://github.com/efabless/volare
