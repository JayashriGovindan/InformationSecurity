# InformationSecurity
## Introduction:
In this lab exercise, the Papyrus modelling environment in Eclipse was used to build model-secured systems in UML with specified functional models and access control policies. B4MSecure was used to generate the necessary B specification for doing the model checking (testing).
In the second lab section, the policy was tested by animating a scenario using the SecureUML model and UML class diagram translation to generate and validate the model with some data and experiment with different scenarios.

## Brief Procedure & Observation:
1. The hospital management system was created with a functional model and then defined the security policy for role based access control of the system. 
2. The B specification for the system's functional model was created using the B4MSecure transformation. 
3. Classes were represented as sets, instances as variables, attributes as functions, associations as relations between instances, and the function as a B operation in the resulting B specification. For example, the validate function was converted to the corresponding MedicalRecord_validate B operation.
4. To further strengthen the B specification, a few more invariants were added. For instance, the B predicate can be used to add a constraint to the system, such as the prohibition on a patient having more than one unvalidated medical record. Similarly simple preconditions and constraints were also added to the UML model's validate() method.
5. The next part was to provide access control policy to the system which started with applying SecureUML policy to the model.
6. It was expanded to include roles like doctor, nurse, and secretary, and users like Mary, Paul, and Martin were given those roles. In these UML model classes that define roles and security users association, stereotypes such as Role and User were applied.
6. The permission model was then added to define the permitted actions by its methods using the permission stereotype.
7. Every time a regeneration of the B specification was required, B4Msecure was run.
8. In order to test the system, some data was added for patient and medical record. After that, the different scenarios can be created and rendered using Animate Machine, which provided the execution history as well as the execution view and state view when an action was carried out. Instantaneously, when the operation is double-clicked and executed in the execution view, the state view is updated and the operation is added to the execution history.
9. B4MSecure helped with overall logical inference on the created model for Hospital System. Following that, during the testing phase, the B specification produced by B4MSecure was used to conduct the model checking.

## Conclusion:
Role-based access control served as the foundation for the lab experiment, with added support for defining authorization constraints in the security policy in addition to the permission model. Through this experiment, it was understood that access control-related information can be specified using UML in the overall program architecture, and that this information can be utilized to automatically develop entire access control facilities.

## References:
1)	Lab Manual: http://vasco.imag.fr/tools/b4msecure/UserManual-2.0.pdf 
2)	SecureUML - A UML-Based Modelling Language for Model-Driven Security: https://dl.acm.org/doi/10.5555/647246.719477 
