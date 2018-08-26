---
swagger: "2.0"
x-collection-name: AWS Storage Gateway Service
x-complete: 1
info:
  title: AWS Storage Gateway Service API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateStorediSCSIVolume:
    get:
      summary: Create Stored SCSI Volume
      description: Creates a volume on a specified gateway.
      operationId: createStorediSCSIVolume
      x-api-path-slug: actioncreatestorediscsivolume-get
      parameters:
      - in: query
        name: DiskId
        description: The unique identifier for the gateway local disk that is configured
          as a stored         volume
        type: string
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      - in: query
        name: NetworkInterfaceId
        description: The network interface of the gateway on which to expose the iSCSI
          target
        type: string
      - in: query
        name: PreserveExistingData
        description: Specify this field as true if you want to preserve the data on
          the local disk
        type: string
      - in: query
        name: SnapshotId
        description: The snapshot ID (e
        type: string
      - in: query
        name: TargetName
        description: The name of the iSCSI target used by initiators to connect to
          the target and as a         suffix for the target ARN
        type: string
      responses:
        200:
          description: OK
      tags:
      - Stored SCSI Volume
  /?Action=DescribeStorediSCSIVolumes:
    get:
      summary: Describe Stored SCSI Volumes
      description: Returns the description of the gateway volumes specified in the
        request.
      operationId: describeStorediSCSIVolumes
      x-api-path-slug: actiondescribestorediscsivolumes-get
      parameters:
      - in: query
        name: VolumeARNs
        description: An array of strings where each string represents the Amazon Resource
          Name (ARN) of a         stored volume
        type: string
      responses:
        200:
          description: OK
      tags:
      - Stored SCSI Volumes
---