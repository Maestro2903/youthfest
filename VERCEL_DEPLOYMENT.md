# Deploying Youth Fest to Vercel

This guide provides step-by-step instructions for deploying the Youth Fest website to Vercel.

## Prerequisites

- A Vercel account (sign up at [vercel.com](https://vercel.com) if you don't have one)
- Git installed on your computer
- Node.js installed on your computer

## Deployment Options

### Option 1: Deploy with Vercel CLI (Recommended for first deployment)

1. **Install Vercel CLI globally**

   ```bash
   npm install -g vercel
   ```

2. **Login to your Vercel account**

   ```bash
   vercel login
   ```

3. **Deploy from the project directory**

   ```bash
   cd /path/to/youthfest-main-4
   vercel
   ```

   Follow the prompts to configure your project:
   - Set up and deploy: Yes
   - Link to existing project: No (for first deployment)
   - Project name: youthfest (or your preferred name)
   - Directory: ./ (current directory)

4. **Deploy to production**

   After testing the preview deployment, deploy to production:

   ```bash
   vercel --prod
   ```

### Option 2: Deploy via GitHub Integration

1. **Push your code to GitHub**

   ```bash
   # Initialize git repository (if not already done)
   git init
   
   # Add all files
   git add .
   
   # Commit changes
   git commit -m "Initial commit"
   
   # Add remote repository (replace with your GitHub repo URL)
   git remote add origin https://github.com/yourusername/youthfest.git
   
   # Push to GitHub
   git push -u origin master
   ```

2. **Import your repository in Vercel**

   - Go to [vercel.com/import](https://vercel.com/import)
   - Select "Import Git Repository"
   - Choose your GitHub account and select the repository
   - Configure project settings (Vercel will auto-detect settings from vercel.json)
   - Click "Deploy"

## Custom Domain Setup

1. Go to your project dashboard in Vercel
2. Navigate to "Settings" > "Domains"
3. Add your custom domain and follow the verification steps

## Continuous Deployment

With GitHub integration, Vercel automatically deploys:
- Preview deployments for every push
- Production deployments when you merge to your main branch

## Environment Variables

If your project requires environment variables:
1. Go to your project dashboard in Vercel
2. Navigate to "Settings" > "Environment Variables"
3. Add your variables for Development, Preview, and Production environments

## Troubleshooting

- **Build Errors**: Check the build logs in your Vercel dashboard
- **Deployment Issues**: Ensure your vercel.json configuration is correct
- **Preview Not Working**: Make sure all assets are properly referenced with relative paths

## Support

If you encounter any issues, refer to the [Vercel documentation](https://vercel.com/docs) or contact Vercel support.