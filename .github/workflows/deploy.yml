###################################################################
#Deploy action

# GitHub displays the names of your workflows on your repository's actions page
name: Bootcamp Deploy Action! 

# Controls when the workflow will run
on:   
  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:
    inputs:
      ghhandle:
        description: 'The GitHub Handle of the user to set up'
        default: 'bootcamp_magician'
        type: string
           
# A workflow run is made up of one or more jobs that can run sequentially or in parallel
jobs:
  # This workflow contains a single job called "build"
  DeployToDev:
    # The type of runner that the job will run on
    runs-on: windows-latest
    environment: Dev
        
    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:
      # Runs a single command using the runners shell
      - name: Deploying To Dev for ${{ inputs.ghhandle }}!
        run: "echo I just deployed to Dev"

  DeployToProd:
    runs-on: windows-latest
    needs: DeployToDev
    environment: Production
    
    steps:
      - name: Deploying To Production for ${{ inputs.ghhandle }}!
        run: "echo I just deployed to Production"
###################################################################
