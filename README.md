Visual Studio 2010 Extension for creating Entity Framework 4.1 (or greater) Entity model code generators.

To install the extension, simply grab the latest release [from the Downloads Page](https://github.com/kavika13/TestableDbContextCodeGen/downloads), extract the Zip file, and run the extension installer.

Use the generators just like you would the existing [`DbContext`](http://msdn.microsoft.com/en-us/library/system.data.entity.dbcontext\(v=VS.103\).aspx) code generators.  Simply right click on your Edmx model and click `Add Code Generation Item...`

The code that gets created has a `DbContext` that is derived from a mockable interface ([Unit of Work Pattern](http://martinfowler.com/eaaCatalog/unitOfWork.html)), which exposes the Entity [Repositories](http://martinfowler.com/eaaCatalog/repository.html) as [`IDbSet<TEntity>`](http://msdn.microsoft.com/en-us/library/gg679233\(v=VS.103\).aspx).

Pretty simple.

See my (currently incompletely) blog entries on the subject:

- [Entity Framework – The Repository and Unit of Work Patterns](http://thehappypath.net/2011/11/11/entity-framework-the-repository-and-unit-of-work-patterns/)
- [More Proof – Repository and Unit of Work](http://thehappypath.net/2011/11/13/more-proof-repository-and-unit-of-work/)
