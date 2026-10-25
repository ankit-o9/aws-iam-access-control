# IAM Implementation Steps

## Step 1: Analyze Current IAM Setup
1. Log in to the AWS Console.
2. 2. Navigate to the IAM dashboard.
   3. 3. Review existing users, groups, and policies.
      4. 4. Document current permission boundaries.
        
         5. ## Step 2: Create IAM Groups
         6. 1. Go to IAM → User Groups → Create Group.
            2. 2. Create the `S3-Support` group.
               3. 3. Create the `EC2-Support` group.
                  4. 4. Create the `EC2-Admin` group.
                    
                     5. ## Step 3: Attach Policies to Groups
                     6. ### S3-Support Group
                     7. - Attach `s3-support-policy.json`.
                        - - Intended permissions: read-only S3 access.
                         
                          - ### EC2-Support Group
                          - - Attach `ec2-support-policy.json`.
                            - - Intended permissions: read-only EC2 access.
                             
                              - ### EC2-Admin Group
                              - - Attach `ec2-admin-policy.json`.
                                - - Intended permissions: full EC2 access.
                                 
                                  - ## Step 4: Create Users and Assign to Groups
                                  - 1. Create test users: `s3-support-user`, `ec2-support-user`, and `ec2-admin-user`.
                                    2. 2. Assign each user to the respective group.
                                       3. 3. Generate console passwords for testing.
                                         
                                          4. ## Step 5: Test Permissions
                                          5. ### Test S3 Support User
                                          6. - [ ] Sign in as `s3-support-user`.
                                             - [ ] - [ ] List S3 buckets (should succeed).
                                             - [ ] - [ ] Download an object (should succeed).
                                             - [ ] - [ ] Delete an object (should fail).
                                            
                                             - [ ] ### Test EC2 Support User
                                             - [ ] - [ ] Sign in as `ec2-support-user`.
                                             - [ ] - [ ] List EC2 instances (should succeed).
                                             - [ ] - [ ] View security groups (should succeed).
                                             - [ ] - [ ] Stop an instance (should fail).
                                            
                                             - [ ] ### Test EC2 Admin User
                                             - [ ] - [ ] Sign in as `ec2-admin-user`.
                                             - [ ] - [ ] List instances (should succeed).
                                             - [ ] - [ ] Stop an instance (should succeed).
                                             - [ ] - [ ] Terminate an instance (should succeed).
                                            
                                             - [ ] ## Step 6: Monitor with CloudTrail
                                             - [ ] 1. Go to CloudTrail → Event history.
                                             - [ ] 2. Filter by username to verify actions.
                                             - [ ] 3. Confirm that only allowed actions appear.
                                            
                                             - [ ] ## Step 7: Documentation and Handoff
                                             - [ ] 1. Document all group policies.
                                             - [ ] 2. Create user login instructions.
                                             - [ ] 3. Provide a testing results summary.
                                             - [ ] 
