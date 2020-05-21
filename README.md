# AngularUnitTest
Karma + Jasmine

Karma --> Test Executor ( Test Suite )
Test bed -> Creating testing modules same as angular.module.ts
Fixture --> Wrapper on the component, to get hold of components including variables, menthods.
debugElement --> get hold of html elements with the help of By library

detectChanges -- internally runs ngOnInit method of a component


```



```
Steps :



1) Set up TestBed --> configure testing modules for TestBed
```
    TestBed.configureTestingModule({
      declarations: [
        HerosComponent,
        HeroComponent
      ],
      providers: [
      { provide: heroService, useValue: mockHeroService }
      ],
      // schemas: [ NO_ERRORS_SCHEMA ]
    })
```
2) Cretae Fixture to get hold of the component
```
fixture = TestBed.createComponent(HersoComponent)
```
3) Create mock service with all the methods
```
mockHeroService = jasmine.createSpyObj(['getHersos', 'addHero', 'deleteHero'])

```
4) Set mock service method to return desired response. HEROS is an Array of object or JSON.
```
mockHeroService.getHeros.and.returnValue(of(HEROS));
```
5) fixture.detectChanges --> to bind the .ts with template file, internally runs ngOnInit method of a component
```
fixture.detectChanges():
```
