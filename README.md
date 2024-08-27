<p align="left">
  <a>
    <img alt="Made With Unity" src="https://img.shields.io/badge/made%20with-Unity-57b9d3.svg?logo=Unity">
  </a>
  <a>
    <img alt="License" src="https://img.shields.io/github/license/wolf-package/object-pooling-unity?logo=github">
  </a>
  <a>
    <img alt="Last Commit" src="https://img.shields.io/github/last-commit/wolf-package/object-pooling-unity?logo=Mapbox&color=orange">
  </a>
  <a>
    <img alt="Repo Size" src="https://img.shields.io/github/repo-size/wolf-package/object-pooling-unity?logo=VirtualBox">
  </a>
  <a>
    <img alt="Last Release" src="https://img.shields.io/github/v/release/wolf-package/object-pooling-unity?include_prereleases&logo=Dropbox&color=yellow">
  </a>
</p>

## What

- Object-Pooling for game unity is very easy to use

## How To Install

### Add the line below to `Packages/manifest.json`

for version `1.0.1`
```csharp
"com.wolf-org.object-pooling":"https://github.com/wolf-org/object-pooling-unity.git#1.0.1",
```
## Use

- Init Pool

```csharp
    Pool.InitPool();
```

- Spawn/DeSpawn Object

```csharp

    public GameObject prefab;

    private GameObject ins;

    void SpawnIns()
    {
        ins = Pool.Spawn(prefab);
    }

    void DeSpawnIns()
    {
        Pool.DeSpawn(ins);
    }

```

Or

```csharp

    public GameObject prefab;

    private GameObject ins;

    void SpawnIns()
    {
        ins = prefab.Spawn();
    }

    void DeSpawnIns()
    {
        ins.DeSpawn();
    }

```