# Win32_Volume


```
class Win32_Volume : CIM_StorageVolume
{
  uint16   Access;
  boolean  Automount;
  uint16   Availability;
  uint64   BlockSize;
  uint64   Capacity;               #Size of the volume in bytes.
  string   Caption;                #String with drive letter path - "C:\"
  boolean  Compressed;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  DirtyBitSet;
  string   DriveLetter;            #String with drive letter - "C:"
  uint32   DriveType;              #Int with drive type
    - 0 (0x0) Unknown
    - 1 (0x1) No Root Directory
    - 2 (0x2) Removable Disk
    - 3 (0x3) Local Disk #One to use to get info from local disks
    - 4 (0x4) Network Drive
    - 5 (0x5) Compact Disk
    - 6 (0x6) RAM Disk
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;             #Filesystem on the disk - "NTFS"
  uint64   FreeSpace;              #Space, in bytes, available on the logical disk
  boolean  IndexingEnabled;
  datetime InstallDate;
  string   Label;                  #Volume name of the logical disk
  uint32   LastErrorCode;
  uint32   MaximumFileNameLength;
  string   Name;                   #Label by which the object is known
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16[] PowerManagementCapabilities;
  boolean  PowerManagementSupported;
  string   Purpose;
  boolean  QuotasEnabled;
  boolean  QuotasIncomplete;
  boolean  QuotasRebuilding;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   SerialNumber;            #Serial num of the volume
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
};

   TypeName: System.Management.ManagementObject#root\cimv2\Win32_Volume

Name                         MemberType    Definition                                                                  
----                         ----------    ----------                                                                  
PSComputerName               AliasProperty PSComputerName = __SERVER                                                   
AddMountPoint                Method        System.Management.ManagementBaseObject AddMountPoint(System.String Direct...
Chkdsk                       Method        System.Management.ManagementBaseObject Chkdsk(System.Boolean FixErrors, S...
Defrag                       Method        System.Management.ManagementBaseObject Defrag(System.Boolean Force)         
DefragAnalysis               Method        System.Management.ManagementBaseObject DefragAnalysis()                     
Dismount                     Method        System.Management.ManagementBaseObject Dismount(System.Boolean Force, Sys...
Format                       Method        System.Management.ManagementBaseObject Format(System.String FileSystem, S...
Mount                        Method        System.Management.ManagementBaseObject Mount()                              
Reset                        Method        System.Management.ManagementBaseObject Reset()                              
SetPowerState                Method        System.Management.ManagementBaseObject SetPowerState(System.UInt16 PowerS...
Access                       Property      uint16 Access {get;set;}                                                    
Automount                    Property      bool Automount {get;set;}                                                   
Availability                 Property      uint16 Availability {get;set;}                                              
BlockSize                    Property      uint64 BlockSize {get;set;}                                                 
BootVolume                   Property      bool BootVolume {get;set;}                                                  
Capacity                     Property      uint64 Capacity {get;set;}                                                  
Caption                      Property      string Caption {get;set;}                                                   
Compressed                   Property      bool Compressed {get;set;}                                                  
ConfigManagerErrorCode       Property      uint32 ConfigManagerErrorCode {get;set;}                                    
ConfigManagerUserConfig      Property      bool ConfigManagerUserConfig {get;set;}                                     
CreationClassName            Property      string CreationClassName {get;set;}                                         
Description                  Property      string Description {get;set;}                                               
DeviceID                     Property      string DeviceID {get;set;}                                                  
DirtyBitSet                  Property      bool DirtyBitSet {get;set;}                                                 
DriveLetter                  Property      string DriveLetter {get;set;}                                               
DriveType                    Property      uint32 DriveType {get;set;}                                                 
ErrorCleared                 Property      bool ErrorCleared {get;set;}                                                
ErrorDescription             Property      string ErrorDescription {get;set;}                                          
ErrorMethodology             Property      string ErrorMethodology {get;set;}                                          
FileSystem                   Property      string FileSystem {get;set;}                                                
FreeSpace                    Property      uint64 FreeSpace {get;set;}                                                 
IndexingEnabled              Property      bool IndexingEnabled {get;set;}                                             
InstallDate                  Property      string InstallDate {get;set;}                                               
Label                        Property      string Label {get;set;}                                                     
LastErrorCode                Property      uint32 LastErrorCode {get;set;}                                             
MaximumFileNameLength        Property      uint32 MaximumFileNameLength {get;set;}                                     
Name                         Property      string Name {get;set;}                                                      
NumberOfBlocks               Property      uint64 NumberOfBlocks {get;set;}                                            
PageFilePresent              Property      bool PageFilePresent {get;set;}                                             
PNPDeviceID                  Property      string PNPDeviceID {get;set;}                                               
PowerManagementCapabilities  Property      uint16[] PowerManagementCapabilities {get;set;}                             
PowerManagementSupported     Property      bool PowerManagementSupported {get;set;}                                    
Purpose                      Property      string Purpose {get;set;}                                                   
QuotasEnabled                Property      bool QuotasEnabled {get;set;}                                               
QuotasIncomplete             Property      bool QuotasIncomplete {get;set;}                                            
QuotasRebuilding             Property      bool QuotasRebuilding {get;set;}                                            
SerialNumber                 Property      uint32 SerialNumber {get;set;}                                              
Status                       Property      string Status {get;set;}                                                    
StatusInfo                   Property      uint16 StatusInfo {get;set;}                                                
SupportsDiskQuotas           Property      bool SupportsDiskQuotas {get;set;}                                          
SupportsFileBasedCompression Property      bool SupportsFileBasedCompression {get;set;}                                
SystemCreationClassName      Property      string SystemCreationClassName {get;set;}                                   
SystemName                   Property      string SystemName {get;set;}                                                
SystemVolume                 Property      bool SystemVolume {get;set;}                                                
__CLASS                      Property      string __CLASS {get;set;}                                                   
__DERIVATION                 Property      string[] __DERIVATION {get;set;}                                            
__DYNASTY                    Property      string __DYNASTY {get;set;}                                                 
__GENUS                      Property      int __GENUS {get;set;}                                                      
__NAMESPACE                  Property      string __NAMESPACE {get;set;}                                               
__PATH                       Property      string __PATH {get;set;}                                                    
__PROPERTY_COUNT             Property      int __PROPERTY_COUNT {get;set;}                                             
__RELPATH                    Property      string __RELPATH {get;set;}                                                 
__SERVER                     Property      string __SERVER {get;set;}                                                  
__SUPERCLASS                 Property      string __SUPERCLASS {get;set;}                                              
ConvertFromDateTime          ScriptMethod  System.Object ConvertFromDateTime();                                        
ConvertToDateTime            ScriptMethod  System.Object ConvertToDateTime();                                          


```
