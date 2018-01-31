## NDRange

- [Upper Level](README.md)

#### Global Size

> > The problem we want to compute should have some dimensionality. For example, compute a kernel on all points in a cube.
>
> > When we execute the kernel we specify up to 3 dimensions.
>
> > We also specify the total problem size in each dimension - this is called the global size.

#### Work Item

> We associate each point in the iteration space with a work-item.

#### Work Groups

> Work-items are grouped into work-groups; work-items within a work-group can share local memory and can synchronize.

#### Local Size

> We can specify the number of work-items in a work-group - this is called the local (work-group) size.
>
> Or the OpenCL run-time can choose the work-group size for you (usually not optimally).

Source of the above quotes: https://github.com/HandsOnOpenCL/Lecture-Slides