#### To use font-awesome in material design
```
<md-input-container class="md-icon-float md-block">
    <md-icon md-font-icon="icon-group" ng-class="icon" class="fa fa-dollar"></md-icon>
    <input ng-model="activity.price" name="unitCost" ng-value="{{ activity.price}}" format="currency">
</md-input-container>
````
