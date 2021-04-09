# .netcorePractice
Practicing Learning .NET CORE using a course in linkedin learning


Concept: Middleware.
-Handling requests:
  A web app is nothing more than just a bunch of functions that gets registered to handle requests in a certain order.
  When a request comes in ASP .net creates a new instance of this pipeline and populates it with these functions.
  Then it gives these functions opportunity to execute their logic in a specific order. These functions don't know anything about each other, they just execute
  Which lets them be able to be reused in other apps. Most methods in ASP .net core are implemented as middleware.

Endpoint.mapget???: https://andrewlock.net/comparing-startup-between-the-asp-net-core-3-templates/ 
  The main difference compared to ASP.NET Core 2.x apps is the conspicuous use of endpoint routing. This was introduced in 2.2, but could only be used for MVC controllers. In 3.0, endpoint routing is the preferred approach, with the most basic setup provided here.

Endpoint routing separates the process of selecting which "endpoint" will execute from the actual running of that endpoint. An endpoint consists of a path pattern, and something to execute when called. It could be an MVC action on a controller or it could be a simple lambda, as shown in this example where we're creating an endpoint using MapGet() for the path /.

The UseRouting() extension method is what looks at the incoming request and decides which endpoint should execute. Any middleware that appears after the UseRouting() call will know which endpoint will run eventually. The UseEndpoints() call is responsible for configuring the endpoints, but also for executing them.


