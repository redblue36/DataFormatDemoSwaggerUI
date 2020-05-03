# OpenapiClient::Position

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | Name of the location site.  | [optional] 
**qualifier** | **String** | Type of Location | [optional] 
**latitude** | **Float** | Value representing latitude in degress and minutes | [optional] 
**longitude** | **Float** | Value representing longitude in degrees and minutes | [optional] 
**accuracy_meters** | **Float** | Accuracy of latitude/longitude within meters. | [optional] 
**altitude_meters** | **Float** | Accuracy of height within meters. | [optional] 
**splc** | **String** | Standard Point Location Code | [optional] 
**address_line1** | **String** | Street, Apt, Suite information | [optional] 
**address_line2** | **String** | Street, Apt #, Suite #, information | [optional] 
**city** | **String** | City name | [optional] 
**state_province** | **String** | State or Province name | [optional] 
**zip_postal** | **String** | Zip code | [optional] 
**country** | **String** | Name of country | [optional] 
**country_code** | **String** | Country code of country | [optional] 
**building_name** | **String** | Building name | [optional] 
**building_floor** | **String** | Building floor | [optional] 
**isle** | **String** | isle 1 | [optional] 
**bin** | **String** | bin 5 | [optional] 
**parking_name** | **String** | Yard/Parking/Any kind of open structure: Lot Name, Floor, Isle, LotId | [optional] 
**level** | **String** | L5 | [optional] 
**lot_id** | **String** | Lot15 | [optional] 

## Code Sample

```ruby
require 'OpenapiClient'

instance = OpenapiClient::Position.new(name: null,
                                 qualifier: null,
                                 latitude: null,
                                 longitude: null,
                                 accuracy_meters: null,
                                 altitude_meters: null,
                                 splc: null,
                                 address_line1: null,
                                 address_line2: null,
                                 city: null,
                                 state_province: null,
                                 zip_postal: null,
                                 country: null,
                                 country_code: null,
                                 building_name: null,
                                 building_floor: null,
                                 isle: null,
                                 bin: null,
                                 parking_name: null,
                                 level: null,
                                 lot_id: null)
```


