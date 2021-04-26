# COVID_BCR_Stephenson

Analysis of processed BCR data from - https://www.nature.com/articles/s41591-021-01329-2

## Download IGV references

https://github.com/zktuong/databases_for_vdj

## BCR sequencing data

We downloaded all the `*.h5ad` files from here: https://www.nature.com/articles/s41591-021-01329-2

Then grabbed the metadata for each of these files here:

```
import glob
import scanpy
for i in glob.glob("*.h5ad"):
    vdj = scanpy.read_h5ad(i)
    vdj.obs.to_csv(i+".csv", index=True)
```

<br><br>