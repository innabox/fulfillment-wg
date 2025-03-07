# Demo 1

This document describes plans for Demo 1 of innabox.

## What we will do

* Create a monolithic Fulfillment Service that allows:
   * Cluster creation from a pre-configured set of Agents
   * Cluster teardown
* Allow cluster to be automatically configured with Observability
* Demonstrate all of this within the MOC

## What we won't do

This is a non-exclusive list.

* Create a GUI
* Configure external storage for the cluster
* Automate bare metal configuration for use within ACM

## Workflow

* Setup
  * Install Fulfillment Service in MOC Demo ACM
  * Configure ESI nodes as Agents within MOC Demo ACM
* Create a cluster
   * User calls Fulfillment Service API to create a cluster order
   * Fulfillment Service creates the hosted cluster
   * Fulfillment Service performs further cluster configuration
      * DNS
      * Observability
* Tear down a cluster
   * User calls Fulfillment Service API to delete a cluster order
   * Fulfillment Service destroys the hosted cluster
   * Fulfillment Service undos any additional configuration related to the hosted cluster

## Tasks

* Develop Fulfillment Service
   * Create Fulfillment API specification
   * Implement the Fulfillment Service
   * Implement a demo client
* Demo
   * Set up environment
   * Deploy the service
   * Record and edit the demo
