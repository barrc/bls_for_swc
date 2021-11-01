# bls_for_swc

1. Register for the BLS API [here](https://data.bls.gov/registrationEngine/)
2. Clone repository `git clone https://github.com/barrc/bls_for_swc`
3. Change directory to bls_for_swc 
4. Create src/passwords.py with 

```
BLS_API_KEY = "your_BLS_key"
```

5. Create conda environment `conda env create --file bls.yml` and activate `conda activate bls`
6. Run `python src/bls_for_swc.py YEAR` and note national index value
   - If you run into problems and need to debug, you can use the debug flag to avoid downloading the data multiple times: `python src/bls_for_swc.py 2020 --debug True` 
7. Copy costRegionalizationCache.txt to swcalculator_home/costData
8. Change national index in CostRegionalizationServiceImpl.java
9. Change year in legends (in Front End)
