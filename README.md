# 3dtiles_validator_testing

1] Implicit tiling

Report with implicit tiling disabled - includes b3dm files validation

```
 $ npx ts-node src\main.ts --tilesetsDirectory D:\dev\github.com\bertt\3dtiles_validator_testing\implicit_tiling_testing\implicit_tiling_disabled
Validating tilesets from D:\dev\github.com\bertt\3dtiles_validator_testing\implicit_tiling_testing\implicit_tiling_disabled matching **/*tileset*.json
Validating tileset D:/dev/github.com/bertt/3dtiles_validator_testing/implicit_tiling_testing/implicit_tiling_disabled/tileset.json
Validation result:
{
  "date": "2023-01-11T12:08:30.961Z",
  "numErrors": 2,
  "numWarnings": 0,
  "numInfos": 0,
  "issues": [
    {
      "type": "PROPERTY_MISSING",
      "path": "/geometricError",
      "message": "The 'geometricError' property is required",
      "severity": "ERROR"
    },
    {
      "type": "CONTENT_VALIDATION_ERROR",
      "path": "content/0_0_0.b3dm",
      "message": "content/0_0_0.b3dm caused validation errors",
      "severity": "ERROR",
      "causes": [
        {
          "type": "BINARY_INVALID_ALIGNMENT",
          "path": "content/0_0_0.b3dm",
          "message": "The byte length must be aligned to 8 bytes",
          "severity": "ERROR"
        }
      ]
    }
  ]
}
Validated 1 files
    1 files with errors
    0 files with warnings
    0 files with infos
```


Report with implicit tiling enabled - no validation of b3dm files?

```
$ npx ts-node src\main.ts --tilesetsDirectory D:\dev\github.com\bertt\3dtiles_validator_testing\implicit_tiling_testing\implicit_tiling_enabled
Validating tilesets from D:\dev\github.com\bertt\3dtiles_validator_testing\implicit_tiling_testing\implicit_tiling_enabled matching **/*tileset*.json
Validating tileset D:/dev/github.com/bertt/3dtiles_validator_testing/implicit_tiling_testing/implicit_tiling_enabled/tileset.json
Validation result:
{
  "date": "2023-01-11T12:09:59.985Z",
  "numErrors": 2,
  "numWarnings": 0,
  "numInfos": 0,
  "issues": [
    {
      "type": "PROPERTY_MISSING",
      "path": "/geometricError",
      "message": "The 'geometricError' property is required",
      "severity": "ERROR"
    },
    {
      "type": "PROPERTY_MISSING",
      "path": "/root/implicitTiling/availableLevels",
      "message": "The 'availableLevels' property is required",
      "severity": "ERROR"
    }
  ]
}
Validated 1 files
    1 files with errors
    0 files with warnings
    0 files with infos
```

