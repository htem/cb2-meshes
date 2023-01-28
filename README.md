# cb2-meshes
Surface renderings of neurons in the paper "Structured cerebellar connectivity supports resilient pattern separation"

## Mesh files

The meshes were primarily used for interactive viewing thus we provide no guarantees for applications beyond that (i.e., analyses) but they are uploaded here in hope that someone might find it useful.

The meshes were computed in chunks and rendered using [Neuroglancer](https://github.com/google/neuroglancer)'s built-in [meshing engine](https://github.com/google/neuroglancer/blob/f8e99ecc5d00805e9d837bac2b7cda2130b9c7c4/python/ext/src/_neuroglancer.cc) first to a precomputed format, stitched together, then converted to [.ply](https://en.wikipedia.org/wiki/PLY_(file_format)) to be viewable with Blender.

Note: see the [Releases](https://github.com/htem/cb2-meshes/releases) page for some neurons that were too big to upload through git.

## Skeleton files

We are also providing the derived skeletons, which were computed using [meshparty](https://github.com/sdorkenw/MeshParty/blob/9bd1661fc4fea160bd561d8e4220fa6be881fb88/docs/guide/skeletons.rst). The skeletons appear correct at first glance, but we did not use these skeletons for analysis in the paper at all. They are only here to make first-pass analyses less painful as computing skeletons on large datasets can be painful, but a more careful validation is needed. We highly recommend researchers to recompute the skeletons using the above meshes or at least read the advantages and disadvantages of the meshparty [method](https://github.com/sdorkenw/MeshParty/blob/9bd1661fc4fea160bd561d8e4220fa6be881fb88/docs/guide/skeletons.rst#disadvantages).

The files are in the [precomputed skeleton format](https://github.com/google/neuroglancer/blob/8432f531c4d8eb421556ec36926a29d9064c2d3c/src/neuroglancer/datasource/precomputed/skeletons.md), JSON-fyed to be human readable. You can try to use CloudVolume to [ingest](https://github.com/seung-lab/cloud-volume/blob/759f3c165f9e853c33324a3e7dd5b449ae7eb261/cloudvolume/skeleton.py#L68) the .json files and [convert them into more standard formats such as .swc files](https://github.com/seung-lab/cloud-volume/blob/759f3c165f9e853c33324a3e7dd5b449ae7eb261/cloudvolume/skeleton.py#L999).

### Skeleton TODO
- [x] Granule cells
- [ ] Mossy fibers
- [ ] Purkinje cells
