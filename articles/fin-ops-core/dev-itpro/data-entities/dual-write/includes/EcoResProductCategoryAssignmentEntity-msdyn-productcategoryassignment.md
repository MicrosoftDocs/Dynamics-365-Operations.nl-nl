## <a name="product-category-assignments-to-msdyn_productcategoryassignments"></a>Toewijzingen van productcategorieën naar msdyn_productcategoryassignments

Deze sjabloon synchroniseert gegevens tussen Finance and Operations-apps en Common Data Service.

Finance and Operations-veld | Toewijzingstype | Ander Dynamics 365-veld | Standaardwaarde
---|---|---|---
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber | 
PRODUCTCATEGORYNAME | = | msdyn_productcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_productcategory.msdyn_hierarchy.msdyn_name | 
PRODUCTNUMBER | >> | msdyn_name | 
