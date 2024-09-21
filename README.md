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

- Ways to get the **SKY130 PDK**:
  - By **locally hardening a TinyTapeout Design** by following  this [TinyTapeout Guide](https://tinytapeout.com/guides/local-hardening/). This document seems to be in a flux while TT is moving to OpenLane2. Few tweaks needed (as of 08/15/24):
    - The recommendation for Python version is 3.11 but my 3.10.12 seems to run fine. Was confirmed by the developers on the discord channel. May make a difference during reporting is what the developers think.
  - Install `python3-tk` to solve _module tkinter not found_ error: `sudo apt install python3-tk`
  - Docker needs to be installed. When installing Docker, you should choose the "_WSL2 integration_" (default) option instead of Hyper-V.
  - **Note** The above option will integrate with the default distro. If you have multiple distros (eg. Ubuntu-20.04 and 22.04) and you are running the hardening on a non-default distro, you need to set that in the Docker settings: `Settings -> Resources -> WSL Integration` and _enable_ the integration for the used distro.

  - By [locally hardeining a TintyTapeout]
Best way to get the PDK compiled is to clone one of efabless templates and run `make setup`
  - https://github.com/efabless/caravel_user_project
  - https://github.com/efabless/caravel_user_project_analog
- It's installed using a tool called `volare` maintained under the efabless repo:
  - https://github.com/efabless/volare
