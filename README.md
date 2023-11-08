#### cadquery deps missing on pypi for arm64 arch

Workaround for [open issue](https://github.com/CadQuery/cadquery/issues/1434)

Wheels built for `cadquery-ocp` and `nlopt` for `arm64` architecture on `macos` available for download. 

Install with poetry
```bash
### install with poetry from wheels
poetry add https://github.com/generativesolutions/cadquery-dist-macos-arm64/releases/download/v0.0.1/cadquery_ocp-7.7.0.1-cp311-cp311-macosx_11_0_arm64.whl
poetry add https://github.com/generativesolutions/cadquery-dist-macos-arm64/releases/download/v0.0.1/nlopt-2.7.1-cp311-cp311-macosx_14_0_arm64.whl 

### install cadquery 
poetry add cadquery

### verify cadquery works locally
poetry run python
>>> import cadquery
>>> cadquery.Workplane('XY').box(1,2,3).toSvg()
```

