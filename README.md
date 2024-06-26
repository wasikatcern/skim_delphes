# skim_delphes

Macro skim_Delphes.C reads any Delphes (.root) file, looks into Delphes Ttree, and saves TLorentzVectors for jets, b-tagged jets, electrons, muons, photons into a smaller file skimmed_delphes.root.

To run this, use the following command while replacing "input.root", "skimmed_delphes" (output file) by your own filenames:

root -l -b 'skim_Delphes.C("input_delphes.root", "skimmed_delphes.root", Center_of_mass_energy_value, cross_section_value[pb])' 

If Center_of_mass_energy_value=13000 GeV & cross_section_value=100[pb], use : 

root -l -b 'skim_Delphes.C("input_delphes.root", "skimmed_delphes.root", 13000, 100)' 

# skim MasterShef (ATLAS) files

Macro skim_MasterShef.C reads any MasterShef (.root) file of ATLAS, looks into "Nominal" Ttree, and saves TLorentzVectors for jets, b-tagged jets, electrons, muons, photons into a smaller file skimmed_delphes.root.

Use this command :

root -l -b 'skim_MasterShef.C("input_MasterShef.root", "skimmed_MasterShef.root", Center_of_mass_energy_value, cross_section_value[pb])' 

if Center_of_mass_energy_value = 13000 GeV  & cross_section_value=100[pb], use :

root -l -b 'skim_MasterShef.C("input_MasterShef.root", "skimmed_MasterShef.root", 13000, 100)'

# Read skimmed file (delphes or MasterShef or PHYSLITE)

Macro read_skimmed_file.C reads the file skimmed_delphes.root (or other formats) and prints all the TLorentzVectors for all events. 

To run this, use the following command while replacing "skimmed_delphes.root"/"skimmed_MasterShef.root"/"skimmed_PHYSLITE.root" by your own file name :

root -l -b 'read_skimmed_file.C("skimmed_delphes.root")'
root -l -b 'read_skimmed_file.C("skimmed_MasterShef.root")'
root -l -b 'read_skimmed_file.C("skimmed_PHYSLITE.root")'

