### Quiz: Chapter 1 – *The Problems with Component-based Rails and Why Today’s Tooling Is More Powerful*  
**Timestamp:** 20250412_15:33:00

#### Multiple Choice Questions

1. What was the original purpose of Ruby gems that created conflict when used for application modularization?
   - [ ] a. Speed optimization  
   - [ ] b. UI theming  
   - [ ] c. Packaging and distribution  
   - [ ] d. Internal configuration management  

2. Why is Packwerk considered a better alternative to gem-based modularization in Rails?
   - [ ] a. It integrates better with JavaScript  
   - [ ] b. It replaces the need for Rake tasks  
   - [ ] c. It enforces modular boundaries inside the app without requiring gems  
   - [ ] d. It generates database schemas  

3. What is a common drawback of using gemspecs in component-based Rails applications?
   - [ ] a. They can't handle JSON  
   - [ ] b. They require versioned deployments  
   - [ ] c. They include unnecessary metadata for packaging  
   - [ ] d. They override test helpers  

4. What is "dependency drift" in the context of component-based Rails?
   - [ ] a. Inconsistent documentation of dependencies  
   - [ ] b. A situation where dependency versions diverge between component and app  
   - [ ] c. The absence of gemspecs  
   - [ ] d. A Rails version upgrade error  

5. Why is it risky for Rails engine components to have their own initializers?
   - [ ] a. They consume more memory  
   - [ ] b. They can modify application-wide behavior unintentionally  
   - [ ] c. They disable routing  
   - [ ] d. They prevent ActiveRecord usage  

6. How does Packwerk treat the "root package"?
   - [ ] a. As a remote dependency  
   - [ ] b. As a gem container  
   - [ ] c. As the default, encompassing the whole application  
   - [ ] d. As a namespaced JSON object  

7. What configuration issue was illustrated by differing parameter wrapping in JSON responses?
   - [ ] a. Bad route design  
   - [ ] b. Configuration drift between dummy apps and the main app  
   - [ ] c. Gemfile corruption  
   - [ ] d. Unused engine routes  

8. Which of the following was *not* a reason cited for why Packwerk is more appealing than CBRA?
   - [ ] a. Fewer initial setup steps  
   - [ ] b. Better CI integration by default  
   - [ ] c. Avoidance of gem-level metadata  
   - [ ] d. More lightweight and Rails-consistent  

9. What does the author suggest about many ideas in his earlier CBRA book?
   - [ ] a. They remain entirely relevant  
   - [ ] b. They need to be rewritten in TypeScript  
   - [ ] c. They can largely be disregarded due to better tooling  
   - [ ] d. They were too advanced for Rails  

10. What broader lesson does the author draw about modularization in large Rails apps?
   - [ ] a. It is best avoided until apps hit 1 million lines of code  
   - [ ] b. Frameworks like Rails should prevent all modular approaches  
   - [ ] c. Modern tooling enables modularity without abandoning Rails conventions  
   - [ ] d. All apps should be converted to engines  

---

### Answer Key with Explanations

1. **c. Packaging and distribution**  
   Gems were intended for packaging and distributing libraries, not for internal modular structure.

2. **c. It enforces modular boundaries inside the app without requiring gems**  
   Packwerk works within the Rails app itself and doesn't rely on gem-based packaging.

3. **c. They include unnecessary metadata for packaging**  
   Gemspecs demand metadata meant for published gems, which is redundant in internal-only use.

4. **b. A situation where dependency versions diverge between component and app**  
   This leads to unpredictable behavior due to mismatched versions.

5. **b. They can modify application-wide behavior unintentionally**  
   Initializers can unintentionally introduce side effects that impact the whole app.

6. **c. As the default, encompassing the whole application**  
   The root package includes the entire app before modularization into smaller packages.

7. **b. Configuration drift between dummy apps and the main app**  
   Different initializer settings in dummy apps vs. main app caused changes in JSON output.

8. **b. Better CI integration by default**  
   While Packwerk simplifies setup, it doesn’t automatically enhance CI integration.

9. **c. They can largely be disregarded due to better tooling**  
   The author suggests Packwerk obsoletes much of his earlier work in CBRA.

10. **c. Modern tooling enables modularity without abandoning Rails conventions**  
   New tools allow developers to modularize while staying aligned with Rails' standard practices.