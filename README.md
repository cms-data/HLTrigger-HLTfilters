# HLTrigger-HLTfilters
Data files for HLTrigger/HLTfilters

Models for ML-based inference using HLT objects, e.g. topological / anomaly triggers

## Anomaly detection
* `hlt_ad_model.pt` used for anomaly detection@HLT, needed by https://github.com/cms-sw/cmssw/pull/49869

## Topological trigger

BDT models (from XGBoost) for classification of HH bbWW (single muon channel) with PFHT, max pnetB tag + HLT muon parameters (pt/tkIso/ecalIso/hcalIso) as used by the TOPO@HLT here: https://github.com/cms-sw/cmssw/pull/50214 
* `HLT_xgb_model_HH2b2W1L_1mu_HLTHT_sorttkisoMupt-absiso_PNetB.json`: model with one muon with the smallest tkIso/pt 
* `HLT_xgb_model_HH2b2W1L_1mu_HLTHT_Mupt-absiso_PNetB.json`: model with one with the largest pt (default sorting)
* `HLT_xgb_model_HH2b2W1L_1mu_HLTHT_Mu1-2pt-absiso_PNetB.json`: model with the two leading pt muon, sorted by pt
